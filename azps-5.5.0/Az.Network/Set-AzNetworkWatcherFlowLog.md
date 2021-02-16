---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkwatcherflowlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkWatcherFlowLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkWatcherFlowLog.md
ms.openlocfilehash: 04a9b4c0ca8b613ce4d4c590572d80a729a65147
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100160596"
---
# <span data-ttu-id="9d32e-101">Set-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="9d32e-101">Set-AzNetworkWatcherFlowLog</span></span>

## <span data-ttu-id="9d32e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9d32e-102">SYNOPSIS</span></span>
<span data-ttu-id="9d32e-103">Aktualisiert die Flussprotokollressource.</span><span class="sxs-lookup"><span data-stu-id="9d32e-103">Updates flow log resource.</span></span>

## <span data-ttu-id="9d32e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9d32e-104">SYNTAX</span></span>

### <span data-ttu-id="9d32e-105">SetByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="9d32e-105">SetByName (Default)</span></span>
```
Set-AzNetworkWatcherFlowLog -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 -TargetResourceId <String> -StorageId <String> -Enabled <Boolean> [-EnableRetention <Boolean>]
 [-RetentionPolicyDays <Int32>] [-FormatType <String>] [-FormatVersion <Int32>] [-Tag <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9d32e-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="9d32e-106">SetByResource</span></span>
```
Set-AzNetworkWatcherFlowLog -NetworkWatcher <PSNetworkWatcher> -Name <String> -TargetResourceId <String>
 -StorageId <String> -Enabled <Boolean> [-EnableRetention <Boolean>] [-RetentionPolicyDays <Int32>]
 [-FormatType <String>] [-FormatVersion <Int32>] [-Tag <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9d32e-107">SetByResourceWithTA</span><span class="sxs-lookup"><span data-stu-id="9d32e-107">SetByResourceWithTA</span></span>
```
Set-AzNetworkWatcherFlowLog -NetworkWatcher <PSNetworkWatcher> -Name <String> -TargetResourceId <String>
 -StorageId <String> -Enabled <Boolean> [-EnableRetention <Boolean>] [-RetentionPolicyDays <Int32>]
 [-FormatType <String>] [-FormatVersion <Int32>] [-EnableTrafficAnalytics]
 [-TrafficAnalyticsWorkspaceId <String>] [-TrafficAnalyticsInterval <Int32>] [-Tag <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9d32e-108">SetByNameWithTA</span><span class="sxs-lookup"><span data-stu-id="9d32e-108">SetByNameWithTA</span></span>
```
Set-AzNetworkWatcherFlowLog -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 -TargetResourceId <String> -StorageId <String> -Enabled <Boolean> [-EnableRetention <Boolean>]
 [-RetentionPolicyDays <Int32>] [-FormatType <String>] [-FormatVersion <Int32>] [-EnableTrafficAnalytics]
 [-TrafficAnalyticsWorkspaceId <String>] [-TrafficAnalyticsInterval <Int32>] [-Tag <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9d32e-109">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="9d32e-109">SetByLocation</span></span>
```
Set-AzNetworkWatcherFlowLog -Location <String> -Name <String> -TargetResourceId <String> -StorageId <String>
 -Enabled <Boolean> [-EnableRetention <Boolean>] [-RetentionPolicyDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9d32e-110">SetByLocationWithTA</span><span class="sxs-lookup"><span data-stu-id="9d32e-110">SetByLocationWithTA</span></span>
```
Set-AzNetworkWatcherFlowLog -Location <String> -Name <String> -TargetResourceId <String> -StorageId <String>
 -Enabled <Boolean> [-EnableRetention <Boolean>] [-RetentionPolicyDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-EnableTrafficAnalytics] [-TrafficAnalyticsWorkspaceId <String>]
 [-TrafficAnalyticsInterval <Int32>] [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9d32e-111">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="9d32e-111">SetByResourceId</span></span>
```
Set-AzNetworkWatcherFlowLog -ResourceId <String> -TargetResourceId <String> -StorageId <String>
 -Enabled <Boolean> [-EnableRetention <Boolean>] [-RetentionPolicyDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9d32e-112">SetByResourceIdWithTA</span><span class="sxs-lookup"><span data-stu-id="9d32e-112">SetByResourceIdWithTA</span></span>
```
Set-AzNetworkWatcherFlowLog -ResourceId <String> -TargetResourceId <String> -StorageId <String>
 -Enabled <Boolean> [-EnableRetention <Boolean>] [-RetentionPolicyDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-EnableTrafficAnalytics] [-TrafficAnalyticsWorkspaceId <String>]
 [-TrafficAnalyticsInterval <Int32>] [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9d32e-113">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="9d32e-113">SetByInputObject</span></span>
```
Set-AzNetworkWatcherFlowLog -InputObject <PSFlowLogResource> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9d32e-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9d32e-114">DESCRIPTION</span></span>
<span data-ttu-id="9d32e-115">Aktualisiert die Flussprotokollressource.</span><span class="sxs-lookup"><span data-stu-id="9d32e-115">Updates flow log resource.</span></span>

## <span data-ttu-id="9d32e-116">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="9d32e-116">EXAMPLES</span></span>

### <span data-ttu-id="9d32e-117">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="9d32e-117">Example 1</span></span>
```powershell
PS C:\> $flowLog = Get-AzNetworkWatcherFlowLog -Location eastus -Name pstest
PS C:\> $flowLog.Enabled = $true
PS C:\> $flowLog.Format.Version = 2
PS C:\> $flowLog | Set-AzNetworkWatcherFlowLog -Force
```

<span data-ttu-id="9d32e-118">Name: pstest-Id: /subscriptions/bbbbbb-bbbb-bbbb-bbbb-bbbb-bbbbbbbb/resourceGroups/NetworkWatcherRG/provid ers/Microsoft.Network/networkWatchers/NetworkWatcher_eastus/FlowLogs/pstest Etag : W/"e939e1e6-1509-4d7a-9e89-1ea532f6f222" ProvisioningState : Succeeded Location : eastus TargetResourceId : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbb/resourceGroups/MyFlowLog/provide rs/Microsoft.Network/networkSecurityGroups/MyNSG StorageId: /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbb-bbbbbbbbbb/resourceGroups/FlowLogsV2Demo/provider s/Microsoft.Storage/storageAccounts/MyStorage Enabled: True RetentionPolicy : { "Days": 0, "Enabled": false } Format : { "Type": "JSON", "Version": 2 } FlowAnalyticsConfiguration: {}</span><span class="sxs-lookup"><span data-stu-id="9d32e-118">Name                       : pstest Id                         : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/provid ers/Microsoft.Network/networkWatchers/NetworkWatcher_eastus/FlowLogs/pstest Etag                       : W/"e939e1e6-1509-4d7a-9e89-1ea532f6f222" ProvisioningState          : Succeeded Location                   : eastus TargetResourceId           : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/MyFlowLog/provide rs/Microsoft.Network/networkSecurityGroups/MyNSG StorageId                  : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/FlowLogsV2Demo/provider s/Microsoft.Storage/storageAccounts/MyStorage Enabled                    : True RetentionPolicy            : { "Days": 0, "Enabled": false } Format                     : { "Type": "JSON", "Version": 2 } FlowAnalyticsConfiguration : {}</span></span>

## <span data-ttu-id="9d32e-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9d32e-119">PARAMETERS</span></span>

### <span data-ttu-id="9d32e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d32e-120">-DefaultProfile</span></span>
<span data-ttu-id="9d32e-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9d32e-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9d32e-122">-Enabled</span><span class="sxs-lookup"><span data-stu-id="9d32e-122">-Enabled</span></span>
<span data-ttu-id="9d32e-123">Zum Aktivieren/Deaktivieren der Flussprotokollierung kennzeichnen.</span><span class="sxs-lookup"><span data-stu-id="9d32e-123">Flag to enable/disable flow logging.</span></span>

```yaml
Type: Boolean
Parameter Sets: SetByName, SetByResource, SetByResourceWithTA, SetByNameWithTA, SetByLocation, SetByLocationWithTA, SetByResourceId, SetByResourceIdWithTA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d32e-124">-EnableRetention</span><span class="sxs-lookup"><span data-stu-id="9d32e-124">-EnableRetention</span></span>
<span data-ttu-id="9d32e-125">Zum Aktivieren/Deaktivieren der Aufbewahrung kennzeichnen.</span><span class="sxs-lookup"><span data-stu-id="9d32e-125">Flag to enable/disable retention.</span></span>

```yaml
Type: Boolean
Parameter Sets: SetByName, SetByResource, SetByResourceWithTA, SetByNameWithTA, SetByLocation, SetByLocationWithTA, SetByResourceId, SetByResourceIdWithTA
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d32e-126">-EnableTrafficAnalytics</span><span class="sxs-lookup"><span data-stu-id="9d32e-126">-EnableTrafficAnalytics</span></span>
<span data-ttu-id="9d32e-127">Kennzeichnen zum Aktivieren/Deaktivieren von TrafficAnalytics</span><span class="sxs-lookup"><span data-stu-id="9d32e-127">Flag to enable/disable TrafficAnalytics</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: SetByResourceWithTA, SetByNameWithTA, SetByLocationWithTA, SetByResourceIdWithTA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d32e-128">-Force</span><span class="sxs-lookup"><span data-stu-id="9d32e-128">-Force</span></span>
<span data-ttu-id="9d32e-129">Bestätigen Sie nicht, wenn Sie eine Ressource überschreiben möchten</span><span class="sxs-lookup"><span data-stu-id="9d32e-129">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="9d32e-130">-FormatType</span><span class="sxs-lookup"><span data-stu-id="9d32e-130">-FormatType</span></span>
<span data-ttu-id="9d32e-131">Der Dateityp des Flussprotokolls.</span><span class="sxs-lookup"><span data-stu-id="9d32e-131">The file type of flow log.</span></span>
<span data-ttu-id="9d32e-132">Der einzige unterstützte Wert ist jetzt "JSON".</span><span class="sxs-lookup"><span data-stu-id="9d32e-132">The only supported value now is 'JSON'.</span></span>

```yaml
Type: String
Parameter Sets: SetByName, SetByResource, SetByResourceWithTA, SetByNameWithTA, SetByLocation, SetByLocationWithTA, SetByResourceId, SetByResourceIdWithTA
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d32e-133">-FormatVersion</span><span class="sxs-lookup"><span data-stu-id="9d32e-133">-FormatVersion</span></span>
<span data-ttu-id="9d32e-134">Die Version (Revision) des Flussprotokolls.</span><span class="sxs-lookup"><span data-stu-id="9d32e-134">The version (revision) of the flow log.</span></span>

```yaml
Type: Int32
Parameter Sets: SetByName, SetByResource, SetByResourceWithTA, SetByNameWithTA, SetByLocation, SetByLocationWithTA, SetByResourceId, SetByResourceIdWithTA
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d32e-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9d32e-135">-InputObject</span></span>
<span data-ttu-id="9d32e-136">Flow lof-Objekt.</span><span class="sxs-lookup"><span data-stu-id="9d32e-136">Flow lof object.</span></span>

```yaml
Type: PSFlowLogResource
Parameter Sets: SetByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9d32e-137">-Location</span><span class="sxs-lookup"><span data-stu-id="9d32e-137">-Location</span></span>
<span data-ttu-id="9d32e-138">Position der Netzwerk-Watcher.</span><span class="sxs-lookup"><span data-stu-id="9d32e-138">Location of the network watcher.</span></span>

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

### <span data-ttu-id="9d32e-139">-Name</span><span class="sxs-lookup"><span data-stu-id="9d32e-139">-Name</span></span>
<span data-ttu-id="9d32e-140">Der Name des Flussprotokolls.</span><span class="sxs-lookup"><span data-stu-id="9d32e-140">The flow log name.</span></span>

```yaml
Type: String
Parameter Sets: SetByName, SetByResource, SetByResourceWithTA, SetByNameWithTA, SetByLocation, SetByLocationWithTA
Aliases: FlowLogName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d32e-141">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="9d32e-141">-NetworkWatcher</span></span>
<span data-ttu-id="9d32e-142">Die Netzwerk-Watcher-Ressource.</span><span class="sxs-lookup"><span data-stu-id="9d32e-142">The network watcher resource.</span></span>

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

### <span data-ttu-id="9d32e-143">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="9d32e-143">-NetworkWatcherName</span></span>
<span data-ttu-id="9d32e-144">Der Name der Netzwerk-Watcher.</span><span class="sxs-lookup"><span data-stu-id="9d32e-144">The name of network watcher.</span></span>

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

### <span data-ttu-id="9d32e-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d32e-145">-ResourceGroupName</span></span>
<span data-ttu-id="9d32e-146">Der Name der Ressourcengruppe "Netzwerk-Watcher".</span><span class="sxs-lookup"><span data-stu-id="9d32e-146">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="9d32e-147">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9d32e-147">-ResourceId</span></span>
<span data-ttu-id="9d32e-148">FlowLog-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="9d32e-148">FlowLog resource ID.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId, SetByResourceIdWithTA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d32e-149">-RetentionPolicyDays</span><span class="sxs-lookup"><span data-stu-id="9d32e-149">-RetentionPolicyDays</span></span>
<span data-ttu-id="9d32e-150">Die Anzahl der Tage, die die Flussprotokolldatensätze beibehalten werden müssen.</span><span class="sxs-lookup"><span data-stu-id="9d32e-150">Number of days to retain flow log records.</span></span>

```yaml
Type: Int32
Parameter Sets: SetByName, SetByResource, SetByResourceWithTA, SetByNameWithTA, SetByLocation, SetByLocationWithTA, SetByResourceId, SetByResourceIdWithTA
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d32e-151">-StorageId</span><span class="sxs-lookup"><span data-stu-id="9d32e-151">-StorageId</span></span>
<span data-ttu-id="9d32e-152">DIE ID des Speicherkontos, das zum Speichern des Flussprotokolls verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9d32e-152">ID of the storage account which is used to store the flow log.</span></span>

```yaml
Type: String
Parameter Sets: SetByName, SetByResource, SetByResourceWithTA, SetByNameWithTA, SetByLocation, SetByLocationWithTA, SetByResourceId, SetByResourceIdWithTA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d32e-153">-Tag</span><span class="sxs-lookup"><span data-stu-id="9d32e-153">-Tag</span></span>
<span data-ttu-id="9d32e-154">Eine Hashtable, die Ressourcentags darstellt.</span><span class="sxs-lookup"><span data-stu-id="9d32e-154">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: SetByName, SetByResource, SetByResourceWithTA, SetByNameWithTA, SetByLocation, SetByLocationWithTA, SetByResourceId, SetByResourceIdWithTA
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d32e-155">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="9d32e-155">-TargetResourceId</span></span>
<span data-ttu-id="9d32e-156">DIE ID der Netzwerksicherheitsgruppe, auf die das Flussprotokoll angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="9d32e-156">ID of network security group to which flow log will be applied.</span></span>

```yaml
Type: String
Parameter Sets: SetByName, SetByResource, SetByResourceWithTA, SetByNameWithTA, SetByLocation, SetByLocationWithTA, SetByResourceId, SetByResourceIdWithTA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d32e-157">-TrafficAnalyticsInterval</span><span class="sxs-lookup"><span data-stu-id="9d32e-157">-TrafficAnalyticsInterval</span></span>
<span data-ttu-id="9d32e-158">Das Intervall in Minuten, das entscheiden würde, wie häufig der Ta-Dienst Flussanalysen erstellen soll.</span><span class="sxs-lookup"><span data-stu-id="9d32e-158">The interval in minutes which would decide how frequently TA service should do flow analytics.</span></span>

```yaml
Type: Int32
Parameter Sets: SetByResourceWithTA, SetByNameWithTA, SetByLocationWithTA, SetByResourceIdWithTA
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d32e-159">-TrafficAnalyticsWorkspaceId</span><span class="sxs-lookup"><span data-stu-id="9d32e-159">-TrafficAnalyticsWorkspaceId</span></span>
<span data-ttu-id="9d32e-160">Ressourcen-ID des angefügten Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="9d32e-160">Resource Id of the attached workspace.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceWithTA, SetByNameWithTA, SetByLocationWithTA, SetByResourceIdWithTA
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d32e-161">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9d32e-161">-Confirm</span></span>
<span data-ttu-id="9d32e-162">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9d32e-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9d32e-163">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="9d32e-163">-WhatIf</span></span>
<span data-ttu-id="9d32e-164">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9d32e-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9d32e-165">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9d32e-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9d32e-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d32e-166">CommonParameters</span></span>
<span data-ttu-id="9d32e-167">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d32e-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d32e-168">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9d32e-168">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d32e-169">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="9d32e-169">INPUTS</span></span>

### <span data-ttu-id="9d32e-170">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="9d32e-170">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="9d32e-171">System.String</span><span class="sxs-lookup"><span data-stu-id="9d32e-171">System.String</span></span>

### <span data-ttu-id="9d32e-172">Microsoft.Azure.Commands.Network.Models.PSFlowLogResource</span><span class="sxs-lookup"><span data-stu-id="9d32e-172">Microsoft.Azure.Commands.Network.Models.PSFlowLogResource</span></span>

## <span data-ttu-id="9d32e-173">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="9d32e-173">OUTPUTS</span></span>

### <span data-ttu-id="9d32e-174">Microsoft.Azure.Commands.Network.Models.PSFlowLogResource</span><span class="sxs-lookup"><span data-stu-id="9d32e-174">Microsoft.Azure.Commands.Network.Models.PSFlowLogResource</span></span>

## <span data-ttu-id="9d32e-175">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="9d32e-175">NOTES</span></span>

## <span data-ttu-id="9d32e-176">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="9d32e-176">RELATED LINKS</span></span>

[<span data-ttu-id="9d32e-177">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="9d32e-177">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="9d32e-178">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="9d32e-178">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="9d32e-179">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="9d32e-179">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="9d32e-180">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="9d32e-180">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="9d32e-181">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="9d32e-181">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="9d32e-182">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="9d32e-182">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="9d32e-183">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="9d32e-183">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="9d32e-184">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="9d32e-184">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="9d32e-185">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="9d32e-185">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="9d32e-186">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="9d32e-186">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="9d32e-187">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="9d32e-187">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="9d32e-188">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="9d32e-188">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="9d32e-189">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="9d32e-189">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="9d32e-190">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="9d32e-190">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="9d32e-191">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="9d32e-191">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="9d32e-192">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="9d32e-192">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="9d32e-193">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="9d32e-193">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="9d32e-194">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="9d32e-194">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="9d32e-195">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="9d32e-195">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="9d32e-196">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="9d32e-196">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="9d32e-197">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="9d32e-197">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="9d32e-198">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="9d32e-198">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="9d32e-199">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="9d32e-199">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="9d32e-200">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="9d32e-200">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="9d32e-201">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="9d32e-201">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="9d32e-202">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="9d32e-202">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="9d32e-203">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="9d32e-203">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)

[<span data-ttu-id="9d32e-204">New-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="9d32e-204">New-AzNetworkWatcherFlowLog</span></span>](./New-AzNetworkWatcherFlowLog.md)

[<span data-ttu-id="9d32e-205">Get-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="9d32e-205">Get-AzNetworkWatcherFlowLog</span></span>](./Get-AzNetworkWatcherFlowLog)

[<span data-ttu-id="9d32e-206">Remove-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="9d32e-206">Remove-AzNetworkWatcherFlowLog</span></span>](./Remove-AzNetworkWatcherFlowLog.md)
