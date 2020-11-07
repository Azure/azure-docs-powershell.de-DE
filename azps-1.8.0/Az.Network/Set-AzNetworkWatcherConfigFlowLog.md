---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkwatcherconfigflowlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkWatcherConfigFlowLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkWatcherConfigFlowLog.md
ms.openlocfilehash: 4a64226f5445c77c262f1c0521a58d4f3f00ac99
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93660190"
---
# <span data-ttu-id="57e2e-101">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="57e2e-101">Set-AzNetworkWatcherConfigFlowLog</span></span>

## <span data-ttu-id="57e2e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="57e2e-102">SYNOPSIS</span></span>
<span data-ttu-id="57e2e-103">Konfiguriert die Fluss Protokollierung für eine Zielressource.</span><span class="sxs-lookup"><span data-stu-id="57e2e-103">Configures flow logging for a target resource.</span></span>

## <span data-ttu-id="57e2e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="57e2e-104">SYNTAX</span></span>

### <span data-ttu-id="57e2e-105">SetFlowlogByResourceWithoutTA (Standard)</span><span class="sxs-lookup"><span data-stu-id="57e2e-105">SetFlowlogByResourceWithoutTA (Default)</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>]
 [-FormatType <String>] [-FormatVersion <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="57e2e-106">SetFlowlogByResourceWithTAByResource</span><span class="sxs-lookup"><span data-stu-id="57e2e-106">SetFlowlogByResourceWithTAByResource</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>]
 [-FormatType <String>] [-FormatVersion <Int32>] [-AsJob] [-EnableTrafficAnalytics]
 -Workspace <IOperationalInsightWorkspace> [-TrafficAnalyticsInterval <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="57e2e-107">SetFlowlogByResourceWithTAByDetails</span><span class="sxs-lookup"><span data-stu-id="57e2e-107">SetFlowlogByResourceWithTAByDetails</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>]
 [-FormatType <String>] [-FormatVersion <Int32>] [-AsJob] [-EnableTrafficAnalytics]
 -WorkspaceResourceId <String> -WorkspaceGUID <String> -WorkspaceLocation <String>
 [-TrafficAnalyticsInterval <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="57e2e-108">SetFlowlogByNameWithTAByResource</span><span class="sxs-lookup"><span data-stu-id="57e2e-108">SetFlowlogByNameWithTAByResource</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>]
 [-RetentionInDays <Int32>] [-FormatType <String>] [-FormatVersion <Int32>] [-AsJob] [-EnableTrafficAnalytics]
 -Workspace <IOperationalInsightWorkspace> [-TrafficAnalyticsInterval <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="57e2e-109">SetFlowlogByNameWithTAByDetails</span><span class="sxs-lookup"><span data-stu-id="57e2e-109">SetFlowlogByNameWithTAByDetails</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>]
 [-RetentionInDays <Int32>] [-FormatType <String>] [-FormatVersion <Int32>] [-AsJob] [-EnableTrafficAnalytics]
 -WorkspaceResourceId <String> -WorkspaceGUID <String> -WorkspaceLocation <String>
 [-TrafficAnalyticsInterval <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="57e2e-110">SetFlowlogByNameWithoutTA</span><span class="sxs-lookup"><span data-stu-id="57e2e-110">SetFlowlogByNameWithoutTA</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>]
 [-RetentionInDays <Int32>] [-FormatType <String>] [-FormatVersion <Int32>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="57e2e-111">SetFlowlogByLocationWithTAByResource</span><span class="sxs-lookup"><span data-stu-id="57e2e-111">SetFlowlogByLocationWithTAByResource</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -Location <String> -TargetResourceId <String> -EnableFlowLog <Boolean>
 -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-AsJob] [-EnableTrafficAnalytics] -Workspace <IOperationalInsightWorkspace>
 [-TrafficAnalyticsInterval <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="57e2e-112">SetFlowlogByLocationWithTAByDetails</span><span class="sxs-lookup"><span data-stu-id="57e2e-112">SetFlowlogByLocationWithTAByDetails</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -Location <String> -TargetResourceId <String> -EnableFlowLog <Boolean>
 -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-AsJob] [-EnableTrafficAnalytics] -WorkspaceResourceId <String>
 -WorkspaceGUID <String> -WorkspaceLocation <String> [-TrafficAnalyticsInterval <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="57e2e-113">SetFlowlogByLocationWithoutTA</span><span class="sxs-lookup"><span data-stu-id="57e2e-113">SetFlowlogByLocationWithoutTA</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -Location <String> -TargetResourceId <String> -EnableFlowLog <Boolean>
 -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="57e2e-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="57e2e-114">DESCRIPTION</span></span>
<span data-ttu-id="57e2e-115">Die Set-AzNetworkWatcherConfigFlowLog konfiguriert die Fluss Protokollierung für eine Zielressource.</span><span class="sxs-lookup"><span data-stu-id="57e2e-115">The Set-AzNetworkWatcherConfigFlowLog configures flow logging for a target resource.</span></span> <span data-ttu-id="57e2e-116">Zu konfigurierende Eigenschaften: gibt an, ob die Fluss Protokollierung für die bereitgestellte Ressource aktiviert ist, das konfigurierte Speicherkonto zum Senden von Protokollen, das Fluss Protokollierungsformat und die Aufbewahrungsrichtlinie für die Protokolle.</span><span class="sxs-lookup"><span data-stu-id="57e2e-116">Properties to configure include: whether or not flow logging is enabled for the resource provided, the configured storage account to send logs, the flow logging format, and the retention policy for the logs.</span></span> <span data-ttu-id="57e2e-117">Zurzeit werden Netzwerk Sicherheitsgruppen für die Fluss Protokollierung unterstützt.</span><span class="sxs-lookup"><span data-stu-id="57e2e-117">Currently Network Security Groups are supported for flow logging.</span></span> 

## <span data-ttu-id="57e2e-118">Beispiele</span><span class="sxs-lookup"><span data-stu-id="57e2e-118">EXAMPLES</span></span>

### <span data-ttu-id="57e2e-119">Beispiel 1: Konfigurieren der Fluss Protokollierung für ein angegebenes NSG</span><span class="sxs-lookup"><span data-stu-id="57e2e-119">Example 1: Configure Flow Logging for a Specified NSG</span></span>
```
PS C:\> $NW = Get-AzNetworkWatcher -ResourceGroupName NetworkWatcherRg -Name NetworkWatcher_westcentralus
PS C:\> $nsg = Get-AzNetworkSecurityGroup -ResourceGroupName NSGRG -Name appNSG
PS C:\> $storageId = "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123"


PS C:\> Set-AzNetworkWatcherConfigFlowLog -NetworkWatcher $NW -TargetResourceId $nsg.Id -EnableFlowLog $true -StorageAccountId $storageID

TargetResourceId : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Network/networkSecurityGroups/appNSG
StorageId        : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123
Enabled          : True
RetentionPolicy  : {
                     "Days": 0,
                     "Enabled": false
                   }
Format           : {
                     "Type ": "Json",
                     "Version": 1
                   }
```

<span data-ttu-id="57e2e-120">In diesem Beispiel wird der Fluss Protokollierungsstatus für eine Netzwerksicherheitsgruppe konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="57e2e-120">In this example we configure flow logging status for a Network Security Group.</span></span> <span data-ttu-id="57e2e-121">In der Antwort sehen wir die angegebene NSG hat die Fluss Protokollierung aktiviert, das Standardformat und keine Aufbewahrungsrichtlinien festgelegt.</span><span class="sxs-lookup"><span data-stu-id="57e2e-121">In the response, we see the specified NSG has flow logging enabled, default format, and no retention policy set.</span></span>

### <span data-ttu-id="57e2e-122">Beispiel 2: Konfigurieren Sie die Fluss Protokollierung für einen angegebenen NSG, und legen Sie die Version der Fluss Protokollierung auf 2 fest.</span><span class="sxs-lookup"><span data-stu-id="57e2e-122">Example 2: Configure Flow Logging for a Specified NSG and set the version of flow logging to 2.</span></span>
```
PS C:\> $NW = Get-AzNetworkWatcher -ResourceGroupName NetworkWatcherRg -Name NetworkWatcher_westcentralus
PS C:\> $nsg = Get-AzNetworkSecurityGroup -ResourceGroupName NSGRG -Name appNSG
PS C:\> $storageId = "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123"


PS C:\> Set-AzNetworkWatcherConfigFlowLog -NetworkWatcher $NW -TargetResourceId $nsg.Id -EnableFlowLog $true -StorageAccountId $storageID -FormatVersion 2

TargetResourceId : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Network/networkSecurityGroups/appNSG
StorageId        : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123
Enabled          : True
RetentionPolicy  : {
                     "Days": 0,
                     "Enabled": false
                   }
Format           : {
                     "Type ": "Json",
                     "Version": 2
                   }
```

<span data-ttu-id="57e2e-123">In diesem Beispiel wird die Fluss Protokollierung in einer Network Security Group (NSG) mit den angegebenen Protokollen der Version 2 konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="57e2e-123">In this example, we configure flow logging on a Network Security Group (NSG) with version 2 logs specified.</span></span> <span data-ttu-id="57e2e-124">In der Antwort sehen wir den angegebenen NSG ist die Fluss Protokollierung aktiviert, das Format ist festgelegt, und es ist keine Aufbewahrungsrichtlinie konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="57e2e-124">In the response, we see the specified NSG has flow logging enabled, the format is set, and there is no retention policy configured.</span></span> <span data-ttu-id="57e2e-125">Wenn der Bereich die von Ihnen bestimmte Version nicht unterstützt, schreibt Network Watcher die standardmäßig unterstützte Version in der Region.</span><span class="sxs-lookup"><span data-stu-id="57e2e-125">If the region does not support version you specificed, Network Watcher will write the default supported version in the region.</span></span>

### <span data-ttu-id="57e2e-126">Beispiel 3: Konfigurieren der Fluss Protokollierung und der Datenverkehrsanalyse für ein angegebenes NSG</span><span class="sxs-lookup"><span data-stu-id="57e2e-126">Example 3: Configure Flow Logging and Traffic Analytics for a Specified NSG</span></span>
```
PS C:\> $NW = Get-AzNetworkWatcher -ResourceGroupName NetworkWatcherRg -Name NetworkWatcher_westcentralus
PS C:\> $nsg = Get-AzNetworkSecurityGroup -ResourceGroupName NSGRG -Name appNSG
PS C:\> $storageId = "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123"
PS C:\> $workspace = Get-AzOperationalInsightsWorkspace -Name WorkspaceName -ResourceGroupName WorkspaceRg


PS C:\> Set-AzNetworkWatcherConfigFlowLog -NetworkWatcher $NW -TargetResourceId $nsg.Id -EnableFlowLog $true -StorageAccountId $storageID -EnableTrafficAnalytics -Workspace $workspace -TrafficAnalyticsInterval 60

TargetResourceId : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Network/networkSecurityGroups/appNSG
StorageId        : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123
Enabled          : True
RetentionPolicy  : {
                     "Days": 0,
                     "Enabled": false
                   }
Format           : {
                     "Type ": "Json",
                     "Version": 1
                   }
FlowAnalyticsConfiguration : {
            "networkWatcherFlowAnalyticsConfiguration": {
              "enabled": true,
              "workspaceId": "bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb",
              "workspaceRegion": "WorkspaceLocation",
              "workspaceResourceId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourcegroups/WorkspaceRg/providers/microsoft.operationalinsights/workspaces/WorkspaceName",
              "TrafficAnalyticsInterval": 60
            }
          }
```

<span data-ttu-id="57e2e-127">In diesem Beispiel konfigurieren wir den Fluss Protokollierungsstatus und die Datenverkehrsanalyse für eine Netzwerksicherheitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="57e2e-127">In this example we configure flow logging status and Traffic Analytics for a Network Security Group.</span></span> <span data-ttu-id="57e2e-128">In der Antwort sehen wir, dass die angegebene NSG-Funktion Datenflussprotokollierung und Datenverkehrsanalyse aktiviert, Standardformat und keine Aufbewahrungsrichtlinie festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="57e2e-128">In the response, we see the specified NSG has flow logging and Traffic Analytics enabled, default format, and no retention policy set.</span></span>

## <span data-ttu-id="57e2e-129">Parameter</span><span class="sxs-lookup"><span data-stu-id="57e2e-129">PARAMETERS</span></span>

### <span data-ttu-id="57e2e-130">-AsJob</span><span class="sxs-lookup"><span data-stu-id="57e2e-130">-AsJob</span></span>
<span data-ttu-id="57e2e-131">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="57e2e-131">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="57e2e-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57e2e-132">-DefaultProfile</span></span>
<span data-ttu-id="57e2e-133">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="57e2e-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="57e2e-134">-EnableFlowLog</span><span class="sxs-lookup"><span data-stu-id="57e2e-134">-EnableFlowLog</span></span>
<span data-ttu-id="57e2e-135">Kennzeichnen, um die Fluss Protokollierung zu aktivieren/deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="57e2e-135">Flag to enable/disable flow logging.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57e2e-136">-EnableRetention</span><span class="sxs-lookup"><span data-stu-id="57e2e-136">-EnableRetention</span></span>
<span data-ttu-id="57e2e-137">Flag zum Aktivieren/Deaktivieren der Aufbewahrung.</span><span class="sxs-lookup"><span data-stu-id="57e2e-137">Flag to enable/disable retention.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57e2e-138">-EnableTrafficAnalytics</span><span class="sxs-lookup"><span data-stu-id="57e2e-138">-EnableTrafficAnalytics</span></span>
<span data-ttu-id="57e2e-139">Flag zum Aktivieren/Deaktivieren der Aufbewahrung.</span><span class="sxs-lookup"><span data-stu-id="57e2e-139">Flag to enable/disable retention.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SetFlowlogByResourceWithTAByResource, SetFlowlogByResourceWithTAByDetails, SetFlowlogByNameWithTAByResource, SetFlowlogByNameWithTAByDetails, SetFlowlogByLocationWithTAByResource, SetFlowlogByLocationWithTAByDetails
Aliases: EnableTA

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57e2e-140">-Formattyp</span><span class="sxs-lookup"><span data-stu-id="57e2e-140">-FormatType</span></span>
<span data-ttu-id="57e2e-141">Der Typ des Fluss Protokollformats.</span><span class="sxs-lookup"><span data-stu-id="57e2e-141">Type of flow log format.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57e2e-142">-FormatVersion</span><span class="sxs-lookup"><span data-stu-id="57e2e-142">-FormatVersion</span></span>
<span data-ttu-id="57e2e-143">Version des Flow Log-Formats.</span><span class="sxs-lookup"><span data-stu-id="57e2e-143">Version of flow log format.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57e2e-144">-Standort</span><span class="sxs-lookup"><span data-stu-id="57e2e-144">-Location</span></span>
<span data-ttu-id="57e2e-145">Der Speicherort des Netzwerkmonitors.</span><span class="sxs-lookup"><span data-stu-id="57e2e-145">Location of the network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetFlowlogByLocationWithTAByResource, SetFlowlogByLocationWithTAByDetails, SetFlowlogByLocationWithoutTA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57e2e-146">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="57e2e-146">-NetworkWatcher</span></span>
<span data-ttu-id="57e2e-147">Die Netzwerk Überwachungsressource.</span><span class="sxs-lookup"><span data-stu-id="57e2e-147">The network watcher resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher
Parameter Sets: SetFlowlogByResourceWithoutTA, SetFlowlogByResourceWithTAByResource, SetFlowlogByResourceWithTAByDetails
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="57e2e-148">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="57e2e-148">-NetworkWatcherName</span></span>
<span data-ttu-id="57e2e-149">Der Name des Netzwerkmonitors.</span><span class="sxs-lookup"><span data-stu-id="57e2e-149">The name of network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetFlowlogByNameWithTAByResource, SetFlowlogByNameWithTAByDetails, SetFlowlogByNameWithoutTA
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="57e2e-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57e2e-150">-ResourceGroupName</span></span>
<span data-ttu-id="57e2e-151">Der Name der Netzwerk Überwachungsressourcen Gruppe.</span><span class="sxs-lookup"><span data-stu-id="57e2e-151">The name of the network watcher resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetFlowlogByNameWithTAByResource, SetFlowlogByNameWithTAByDetails, SetFlowlogByNameWithoutTA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57e2e-152">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="57e2e-152">-RetentionInDays</span></span>
<span data-ttu-id="57e2e-153">Die Anzahl der Tage, an denen Fluss Protokolldatensätze beibehalten werden sollen.</span><span class="sxs-lookup"><span data-stu-id="57e2e-153">Number of days to retain flow log records.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57e2e-154">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="57e2e-154">-StorageAccountId</span></span>
<span data-ttu-id="57e2e-155">Die ID des speicherkontos, das zum Speichern des Fluss Protokolls verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="57e2e-155">ID of the storage account which is used to store the flow log.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57e2e-156">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="57e2e-156">-TargetResourceId</span></span>
<span data-ttu-id="57e2e-157">Die Ziel Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="57e2e-157">The target resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57e2e-158">-TrafficAnalyticsInterval</span><span class="sxs-lookup"><span data-stu-id="57e2e-158">-TrafficAnalyticsInterval</span></span>
<span data-ttu-id="57e2e-159">Ruft das Intervall (in Minuten) ab, das entscheiden würde, wie häufig der TA-Dienst Flussanalyse durchführen soll, oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="57e2e-159">Gets or sets the interval (in minutes) which would decide how frequently TA service should do flow analytics.</span></span>

```yaml
Type: System.Int32
Parameter Sets: SetFlowlogByResourceWithTAByResource, SetFlowlogByResourceWithTAByDetails, SetFlowlogByNameWithTAByResource, SetFlowlogByNameWithTAByDetails, SetFlowlogByLocationWithTAByResource, SetFlowlogByLocationWithTAByDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57e2e-160">– Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="57e2e-160">-Workspace</span></span>
<span data-ttu-id="57e2e-161">Das WS-Objekt, das zum Speichern der Daten zur Datenverkehrsanalyse verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="57e2e-161">The WS object which is used to store the traffic analytics data.</span></span>

```yaml
Type: Microsoft.Azure.Management.Internal.Network.Common.IOperationalInsightWorkspace
Parameter Sets: SetFlowlogByResourceWithTAByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Management.Internal.Network.Common.IOperationalInsightWorkspace
Parameter Sets: SetFlowlogByNameWithTAByResource, SetFlowlogByLocationWithTAByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57e2e-162">-WorkspaceGUID</span><span class="sxs-lookup"><span data-stu-id="57e2e-162">-WorkspaceGUID</span></span>
<span data-ttu-id="57e2e-163">Die GUID des WS, die zum Speichern der Daten zur Datenverkehrsanalyse verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="57e2e-163">GUID of the WS which is used to store the traffic analytics data.</span></span>

```yaml
Type: System.String
Parameter Sets: SetFlowlogByResourceWithTAByDetails, SetFlowlogByNameWithTAByDetails, SetFlowlogByLocationWithTAByDetails
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57e2e-164">-WorkspaceLocation</span><span class="sxs-lookup"><span data-stu-id="57e2e-164">-WorkspaceLocation</span></span>
<span data-ttu-id="57e2e-165">Der Azure-Bereich des WS, der zum Speichern der Daten für die Datenverkehrsanalyse verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="57e2e-165">Azure Region of the WS which is used to store the traffic analytics data.</span></span>

```yaml
Type: System.String
Parameter Sets: SetFlowlogByResourceWithTAByDetails, SetFlowlogByNameWithTAByDetails, SetFlowlogByLocationWithTAByDetails
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57e2e-166">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="57e2e-166">-WorkspaceResourceId</span></span>
<span data-ttu-id="57e2e-167">Das Abonnement des WS, das zum Speichern der Daten zur Datenverkehrsanalyse verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="57e2e-167">Subscription of the WS which is used to store the traffic analytics data.</span></span>

```yaml
Type: System.String
Parameter Sets: SetFlowlogByResourceWithTAByDetails, SetFlowlogByNameWithTAByDetails, SetFlowlogByLocationWithTAByDetails
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57e2e-168">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="57e2e-168">-Confirm</span></span>
<span data-ttu-id="57e2e-169">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="57e2e-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="57e2e-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57e2e-170">-WhatIf</span></span>
<span data-ttu-id="57e2e-171">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="57e2e-171">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="57e2e-172">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="57e2e-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="57e2e-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57e2e-173">CommonParameters</span></span>
<span data-ttu-id="57e2e-174">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57e2e-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57e2e-175">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57e2e-175">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57e2e-176">Eingaben</span><span class="sxs-lookup"><span data-stu-id="57e2e-176">INPUTS</span></span>

### <span data-ttu-id="57e2e-177">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="57e2e-177">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="57e2e-178">System. String</span><span class="sxs-lookup"><span data-stu-id="57e2e-178">System.String</span></span>

### <span data-ttu-id="57e2e-179">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="57e2e-179">System.Boolean</span></span>

### <span data-ttu-id="57e2e-180">System. Int32</span><span class="sxs-lookup"><span data-stu-id="57e2e-180">System.Int32</span></span>

### <span data-ttu-id="57e2e-181">System. Nullable ' 1 [[System. Int32, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="57e2e-181">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="57e2e-182">Microsoft. Azure. Management. Internal. Network. Common. IOperationalInsightWorkspace</span><span class="sxs-lookup"><span data-stu-id="57e2e-182">Microsoft.Azure.Management.Internal.Network.Common.IOperationalInsightWorkspace</span></span>

## <span data-ttu-id="57e2e-183">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="57e2e-183">OUTPUTS</span></span>

### <span data-ttu-id="57e2e-184">Microsoft. Azure. Commands. Network. Models. PSFlowLog</span><span class="sxs-lookup"><span data-stu-id="57e2e-184">Microsoft.Azure.Commands.Network.Models.PSFlowLog</span></span>

## <span data-ttu-id="57e2e-185">Notizen</span><span class="sxs-lookup"><span data-stu-id="57e2e-185">NOTES</span></span>
<span data-ttu-id="57e2e-186">Schlüsselwörter: Azure, azurerm, arm, Resource, Verwaltung, Manager, Netzwerk, Netzwerk, Watcher, Fluss, Protokolle, flowlog, Protokollierung</span><span class="sxs-lookup"><span data-stu-id="57e2e-186">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, flow, logs, flowlog, logging</span></span>

## <span data-ttu-id="57e2e-187">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="57e2e-187">RELATED LINKS</span></span>

[<span data-ttu-id="57e2e-188">Neu – AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="57e2e-188">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="57e2e-189">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="57e2e-189">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="57e2e-190">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="57e2e-190">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="57e2e-191">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="57e2e-191">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="57e2e-192">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="57e2e-192">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="57e2e-193">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="57e2e-193">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="57e2e-194">Anfang-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="57e2e-194">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="57e2e-195">Neu – AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="57e2e-195">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="57e2e-196">Neu – AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="57e2e-196">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="57e2e-197">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="57e2e-197">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="57e2e-198">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="57e2e-198">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="57e2e-199">Stopp-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="57e2e-199">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="57e2e-200">Neu – AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="57e2e-200">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="57e2e-201">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="57e2e-201">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="57e2e-202">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="57e2e-202">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="57e2e-203">Stopp-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="57e2e-203">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="57e2e-204">Anfang-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="57e2e-204">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="57e2e-205">Satz-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="57e2e-205">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="57e2e-206">Satz-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="57e2e-206">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="57e2e-207">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="57e2e-207">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="57e2e-208">Neu – AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="57e2e-208">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="57e2e-209">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="57e2e-209">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="57e2e-210">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="57e2e-210">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="57e2e-211">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="57e2e-211">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="57e2e-212">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="57e2e-212">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="57e2e-213">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="57e2e-213">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="57e2e-214">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="57e2e-214">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
