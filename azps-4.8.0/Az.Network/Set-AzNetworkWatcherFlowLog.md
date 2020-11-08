---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkwatcherflowlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkWatcherFlowLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkWatcherFlowLog.md
ms.openlocfilehash: 04a9b4c0ca8b613ce4d4c590572d80a729a65147
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94173174"
---
# <span data-ttu-id="d5c95-101">Set-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="d5c95-101">Set-AzNetworkWatcherFlowLog</span></span>

## <span data-ttu-id="d5c95-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d5c95-102">SYNOPSIS</span></span>
<span data-ttu-id="d5c95-103">Update-Flow-Log-Ressource.</span><span class="sxs-lookup"><span data-stu-id="d5c95-103">Updates flow log resource.</span></span>

## <span data-ttu-id="d5c95-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d5c95-104">SYNTAX</span></span>

### <span data-ttu-id="d5c95-105">SetByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="d5c95-105">SetByName (Default)</span></span>
```
Set-AzNetworkWatcherFlowLog -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 -TargetResourceId <String> -StorageId <String> -Enabled <Boolean> [-EnableRetention <Boolean>]
 [-RetentionPolicyDays <Int32>] [-FormatType <String>] [-FormatVersion <Int32>] [-Tag <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d5c95-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="d5c95-106">SetByResource</span></span>
```
Set-AzNetworkWatcherFlowLog -NetworkWatcher <PSNetworkWatcher> -Name <String> -TargetResourceId <String>
 -StorageId <String> -Enabled <Boolean> [-EnableRetention <Boolean>] [-RetentionPolicyDays <Int32>]
 [-FormatType <String>] [-FormatVersion <Int32>] [-Tag <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d5c95-107">SetByResourceWithTA</span><span class="sxs-lookup"><span data-stu-id="d5c95-107">SetByResourceWithTA</span></span>
```
Set-AzNetworkWatcherFlowLog -NetworkWatcher <PSNetworkWatcher> -Name <String> -TargetResourceId <String>
 -StorageId <String> -Enabled <Boolean> [-EnableRetention <Boolean>] [-RetentionPolicyDays <Int32>]
 [-FormatType <String>] [-FormatVersion <Int32>] [-EnableTrafficAnalytics]
 [-TrafficAnalyticsWorkspaceId <String>] [-TrafficAnalyticsInterval <Int32>] [-Tag <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d5c95-108">SetByNameWithTA</span><span class="sxs-lookup"><span data-stu-id="d5c95-108">SetByNameWithTA</span></span>
```
Set-AzNetworkWatcherFlowLog -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 -TargetResourceId <String> -StorageId <String> -Enabled <Boolean> [-EnableRetention <Boolean>]
 [-RetentionPolicyDays <Int32>] [-FormatType <String>] [-FormatVersion <Int32>] [-EnableTrafficAnalytics]
 [-TrafficAnalyticsWorkspaceId <String>] [-TrafficAnalyticsInterval <Int32>] [-Tag <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d5c95-109">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="d5c95-109">SetByLocation</span></span>
```
Set-AzNetworkWatcherFlowLog -Location <String> -Name <String> -TargetResourceId <String> -StorageId <String>
 -Enabled <Boolean> [-EnableRetention <Boolean>] [-RetentionPolicyDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d5c95-110">SetByLocationWithTA</span><span class="sxs-lookup"><span data-stu-id="d5c95-110">SetByLocationWithTA</span></span>
```
Set-AzNetworkWatcherFlowLog -Location <String> -Name <String> -TargetResourceId <String> -StorageId <String>
 -Enabled <Boolean> [-EnableRetention <Boolean>] [-RetentionPolicyDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-EnableTrafficAnalytics] [-TrafficAnalyticsWorkspaceId <String>]
 [-TrafficAnalyticsInterval <Int32>] [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d5c95-111">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="d5c95-111">SetByResourceId</span></span>
```
Set-AzNetworkWatcherFlowLog -ResourceId <String> -TargetResourceId <String> -StorageId <String>
 -Enabled <Boolean> [-EnableRetention <Boolean>] [-RetentionPolicyDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d5c95-112">SetByResourceIdWithTA</span><span class="sxs-lookup"><span data-stu-id="d5c95-112">SetByResourceIdWithTA</span></span>
```
Set-AzNetworkWatcherFlowLog -ResourceId <String> -TargetResourceId <String> -StorageId <String>
 -Enabled <Boolean> [-EnableRetention <Boolean>] [-RetentionPolicyDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-EnableTrafficAnalytics] [-TrafficAnalyticsWorkspaceId <String>]
 [-TrafficAnalyticsInterval <Int32>] [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d5c95-113">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="d5c95-113">SetByInputObject</span></span>
```
Set-AzNetworkWatcherFlowLog -InputObject <PSFlowLogResource> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d5c95-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d5c95-114">DESCRIPTION</span></span>
<span data-ttu-id="d5c95-115">Update-Flow-Log-Ressource.</span><span class="sxs-lookup"><span data-stu-id="d5c95-115">Updates flow log resource.</span></span>

## <span data-ttu-id="d5c95-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d5c95-116">EXAMPLES</span></span>

### <span data-ttu-id="d5c95-117">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d5c95-117">Example 1</span></span>
```powershell
PS C:\> $flowLog = Get-AzNetworkWatcherFlowLog -Location eastus -Name pstest
PS C:\> $flowLog.Enabled = $true
PS C:\> $flowLog.Format.Version = 2
PS C:\> $flowLog | Set-AzNetworkWatcherFlowLog -Force
```

<span data-ttu-id="d5c95-118">Name: pstest-ID:/Subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/provid ERS/Microsoft. Network/networkWatchers/NetworkWatcher_eastus/flowlogs/pstest ETag: W/"e939e1e6-1509-4d7a-9e89-1ea532f6f222" ProvisioningState: succeeded Location: eastus TargetResourceId:/Subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/MyFlowLog/provide RS/Microsoft. Network/networkSecurityGroups/MyNSG Speicher-Nr:/Subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/FlowLogsV2Demo/Provider s/Microsoft. Storage/storageAccounts/mystorage aktiviert: true RetentionPolicy: {"Days": 0; "Enabled": false} Format: {"Typ": "JSON"; "Version": 2} FlowAnalyticsConfiguration: {}</span><span class="sxs-lookup"><span data-stu-id="d5c95-118">Name                       : pstest Id                         : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/provid ers/Microsoft.Network/networkWatchers/NetworkWatcher_eastus/FlowLogs/pstest Etag                       : W/"e939e1e6-1509-4d7a-9e89-1ea532f6f222" ProvisioningState          : Succeeded Location                   : eastus TargetResourceId           : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/MyFlowLog/provide rs/Microsoft.Network/networkSecurityGroups/MyNSG StorageId                  : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/FlowLogsV2Demo/provider s/Microsoft.Storage/storageAccounts/MyStorage Enabled                    : True RetentionPolicy            : { "Days": 0, "Enabled": false } Format                     : { "Type": "JSON", "Version": 2 } FlowAnalyticsConfiguration : {}</span></span>

## <span data-ttu-id="d5c95-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="d5c95-119">PARAMETERS</span></span>

### <span data-ttu-id="d5c95-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5c95-120">-DefaultProfile</span></span>
<span data-ttu-id="d5c95-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d5c95-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d5c95-122">-Aktiviert</span><span class="sxs-lookup"><span data-stu-id="d5c95-122">-Enabled</span></span>
<span data-ttu-id="d5c95-123">Kennzeichnen, um die Fluss Protokollierung zu aktivieren/deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="d5c95-123">Flag to enable/disable flow logging.</span></span>

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

### <span data-ttu-id="d5c95-124">-EnableRetention</span><span class="sxs-lookup"><span data-stu-id="d5c95-124">-EnableRetention</span></span>
<span data-ttu-id="d5c95-125">Flag zum Aktivieren/Deaktivieren der Aufbewahrung.</span><span class="sxs-lookup"><span data-stu-id="d5c95-125">Flag to enable/disable retention.</span></span>

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

### <span data-ttu-id="d5c95-126">-EnableTrafficAnalytics</span><span class="sxs-lookup"><span data-stu-id="d5c95-126">-EnableTrafficAnalytics</span></span>
<span data-ttu-id="d5c95-127">Flag zum Aktivieren/Deaktivieren von TrafficAnalytics</span><span class="sxs-lookup"><span data-stu-id="d5c95-127">Flag to enable/disable TrafficAnalytics</span></span>

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

### <span data-ttu-id="d5c95-128">-Force</span><span class="sxs-lookup"><span data-stu-id="d5c95-128">-Force</span></span>
<span data-ttu-id="d5c95-129">Keine Bestätigung anfordern, wenn Sie eine Ressource überschreiben möchten</span><span class="sxs-lookup"><span data-stu-id="d5c95-129">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="d5c95-130">-Formattyp</span><span class="sxs-lookup"><span data-stu-id="d5c95-130">-FormatType</span></span>
<span data-ttu-id="d5c95-131">Der Dateityp des Fluss Protokolls.</span><span class="sxs-lookup"><span data-stu-id="d5c95-131">The file type of flow log.</span></span>
<span data-ttu-id="d5c95-132">Der einzige unterstützte Wert ist jetzt "JSON".</span><span class="sxs-lookup"><span data-stu-id="d5c95-132">The only supported value now is 'JSON'.</span></span>

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

### <span data-ttu-id="d5c95-133">-FormatVersion</span><span class="sxs-lookup"><span data-stu-id="d5c95-133">-FormatVersion</span></span>
<span data-ttu-id="d5c95-134">Die Version (Revision) des Fluss Protokolls.</span><span class="sxs-lookup"><span data-stu-id="d5c95-134">The version (revision) of the flow log.</span></span>

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

### <span data-ttu-id="d5c95-135">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="d5c95-135">-InputObject</span></span>
<span data-ttu-id="d5c95-136">Flow-Objekt.</span><span class="sxs-lookup"><span data-stu-id="d5c95-136">Flow lof object.</span></span>

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

### <span data-ttu-id="d5c95-137">-Standort</span><span class="sxs-lookup"><span data-stu-id="d5c95-137">-Location</span></span>
<span data-ttu-id="d5c95-138">Der Speicherort des Netzwerkmonitors.</span><span class="sxs-lookup"><span data-stu-id="d5c95-138">Location of the network watcher.</span></span>

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

### <span data-ttu-id="d5c95-139">-Name</span><span class="sxs-lookup"><span data-stu-id="d5c95-139">-Name</span></span>
<span data-ttu-id="d5c95-140">Der Name des Fluss Protokolls.</span><span class="sxs-lookup"><span data-stu-id="d5c95-140">The flow log name.</span></span>

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

### <span data-ttu-id="d5c95-141">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d5c95-141">-NetworkWatcher</span></span>
<span data-ttu-id="d5c95-142">Die Netzwerk Überwachungsressource.</span><span class="sxs-lookup"><span data-stu-id="d5c95-142">The network watcher resource.</span></span>

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

### <span data-ttu-id="d5c95-143">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="d5c95-143">-NetworkWatcherName</span></span>
<span data-ttu-id="d5c95-144">Der Name des Netzwerkmonitors.</span><span class="sxs-lookup"><span data-stu-id="d5c95-144">The name of network watcher.</span></span>

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

### <span data-ttu-id="d5c95-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5c95-145">-ResourceGroupName</span></span>
<span data-ttu-id="d5c95-146">Der Name der Netzwerk Überwachungsressourcen Gruppe.</span><span class="sxs-lookup"><span data-stu-id="d5c95-146">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="d5c95-147">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="d5c95-147">-ResourceId</span></span>
<span data-ttu-id="d5c95-148">FlowLog-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="d5c95-148">FlowLog resource ID.</span></span>

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

### <span data-ttu-id="d5c95-149">-RetentionPolicyDays</span><span class="sxs-lookup"><span data-stu-id="d5c95-149">-RetentionPolicyDays</span></span>
<span data-ttu-id="d5c95-150">Die Anzahl der Tage, an denen Fluss Protokolldatensätze beibehalten werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d5c95-150">Number of days to retain flow log records.</span></span>

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

### <span data-ttu-id="d5c95-151">-Speicher-Nr</span><span class="sxs-lookup"><span data-stu-id="d5c95-151">-StorageId</span></span>
<span data-ttu-id="d5c95-152">Die ID des speicherkontos, das zum Speichern des Fluss Protokolls verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d5c95-152">ID of the storage account which is used to store the flow log.</span></span>

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

### <span data-ttu-id="d5c95-153">-Tag</span><span class="sxs-lookup"><span data-stu-id="d5c95-153">-Tag</span></span>
<span data-ttu-id="d5c95-154">Eine Hashtable, die Ressourcen Tags darstellt.</span><span class="sxs-lookup"><span data-stu-id="d5c95-154">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="d5c95-155">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="d5c95-155">-TargetResourceId</span></span>
<span data-ttu-id="d5c95-156">Die ID der Netzwerksicherheitsgruppe, auf die das Fluss Protokoll angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="d5c95-156">ID of network security group to which flow log will be applied.</span></span>

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

### <span data-ttu-id="d5c95-157">-TrafficAnalyticsInterval</span><span class="sxs-lookup"><span data-stu-id="d5c95-157">-TrafficAnalyticsInterval</span></span>
<span data-ttu-id="d5c95-158">Das Intervall in Minuten, das entscheiden würde, wie häufig der TA-Dienst Flussanalyse ausführen soll.</span><span class="sxs-lookup"><span data-stu-id="d5c95-158">The interval in minutes which would decide how frequently TA service should do flow analytics.</span></span>

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

### <span data-ttu-id="d5c95-159">-TrafficAnalyticsWorkspaceId</span><span class="sxs-lookup"><span data-stu-id="d5c95-159">-TrafficAnalyticsWorkspaceId</span></span>
<span data-ttu-id="d5c95-160">Ressourcen-ID des angefügten Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="d5c95-160">Resource Id of the attached workspace.</span></span>

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

### <span data-ttu-id="d5c95-161">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d5c95-161">-Confirm</span></span>
<span data-ttu-id="d5c95-162">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d5c95-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d5c95-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d5c95-163">-WhatIf</span></span>
<span data-ttu-id="d5c95-164">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d5c95-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d5c95-165">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d5c95-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d5c95-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5c95-166">CommonParameters</span></span>
<span data-ttu-id="d5c95-167">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5c95-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5c95-168">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d5c95-168">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5c95-169">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d5c95-169">INPUTS</span></span>

### <span data-ttu-id="d5c95-170">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d5c95-170">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="d5c95-171">System. String</span><span class="sxs-lookup"><span data-stu-id="d5c95-171">System.String</span></span>

### <span data-ttu-id="d5c95-172">Microsoft. Azure. Commands. Network. Models. PSFlowLogResource</span><span class="sxs-lookup"><span data-stu-id="d5c95-172">Microsoft.Azure.Commands.Network.Models.PSFlowLogResource</span></span>

## <span data-ttu-id="d5c95-173">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d5c95-173">OUTPUTS</span></span>

### <span data-ttu-id="d5c95-174">Microsoft. Azure. Commands. Network. Models. PSFlowLogResource</span><span class="sxs-lookup"><span data-stu-id="d5c95-174">Microsoft.Azure.Commands.Network.Models.PSFlowLogResource</span></span>

## <span data-ttu-id="d5c95-175">Notizen</span><span class="sxs-lookup"><span data-stu-id="d5c95-175">NOTES</span></span>

## <span data-ttu-id="d5c95-176">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d5c95-176">RELATED LINKS</span></span>

[<span data-ttu-id="d5c95-177">Neu – AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d5c95-177">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="d5c95-178">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d5c95-178">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="d5c95-179">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d5c95-179">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="d5c95-180">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="d5c95-180">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="d5c95-181">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="d5c95-181">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="d5c95-182">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="d5c95-182">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="d5c95-183">Anfang-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="d5c95-183">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="d5c95-184">Neu – AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d5c95-184">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d5c95-185">Neu – AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="d5c95-185">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="d5c95-186">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d5c95-186">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d5c95-187">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d5c95-187">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d5c95-188">Stopp-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d5c95-188">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d5c95-189">Neu – AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="d5c95-189">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="d5c95-190">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="d5c95-190">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="d5c95-191">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="d5c95-191">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="d5c95-192">Stopp-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d5c95-192">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d5c95-193">Anfang-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d5c95-193">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d5c95-194">Satz-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d5c95-194">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d5c95-195">Satz-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="d5c95-195">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="d5c95-196">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d5c95-196">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d5c95-197">Neu – AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d5c95-197">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d5c95-198">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="d5c95-198">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="d5c95-199">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="d5c95-199">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="d5c95-200">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="d5c95-200">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="d5c95-201">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="d5c95-201">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="d5c95-202">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="d5c95-202">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="d5c95-203">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d5c95-203">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)

[<span data-ttu-id="d5c95-204">Neu – AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="d5c95-204">New-AzNetworkWatcherFlowLog</span></span>](./New-AzNetworkWatcherFlowLog.md)

[<span data-ttu-id="d5c95-205">Get-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="d5c95-205">Get-AzNetworkWatcherFlowLog</span></span>](./Get-AzNetworkWatcherFlowLog)

[<span data-ttu-id="d5c95-206">Remove-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="d5c95-206">Remove-AzNetworkWatcherFlowLog</span></span>](./Remove-AzNetworkWatcherFlowLog.md)
