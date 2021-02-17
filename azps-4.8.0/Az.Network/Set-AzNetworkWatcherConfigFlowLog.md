---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkwatcherconfigflowlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkWatcherConfigFlowLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkWatcherConfigFlowLog.md
ms.openlocfilehash: afa73cab1f0e66ecc9388b9fb2c536ca50bc609d
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/14/2021
ms.locfileid: "100415426"
---
# <span data-ttu-id="7d7da-101">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="7d7da-101">Set-AzNetworkWatcherConfigFlowLog</span></span>

## <span data-ttu-id="7d7da-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7d7da-102">SYNOPSIS</span></span>
<span data-ttu-id="7d7da-103">Konfiguriert die Flussprotokollierung für eine Zielressource.</span><span class="sxs-lookup"><span data-stu-id="7d7da-103">Configures flow logging for a target resource.</span></span>

## <span data-ttu-id="7d7da-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7d7da-104">SYNTAX</span></span>

### <span data-ttu-id="7d7da-105">SetFlowlogByResourceWithoutTA (Standard)</span><span class="sxs-lookup"><span data-stu-id="7d7da-105">SetFlowlogByResourceWithoutTA (Default)</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>]
 [-FormatType <String>] [-FormatVersion <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d7da-106">SetFlowlogByResourceWithTAByResource</span><span class="sxs-lookup"><span data-stu-id="7d7da-106">SetFlowlogByResourceWithTAByResource</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>]
 [-FormatType <String>] [-FormatVersion <Int32>] [-AsJob] [-EnableTrafficAnalytics]
 -Workspace <IOperationalInsightWorkspace> [-TrafficAnalyticsInterval <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d7da-107">SetFlowlogByResourceWithTAByDetails</span><span class="sxs-lookup"><span data-stu-id="7d7da-107">SetFlowlogByResourceWithTAByDetails</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>]
 [-FormatType <String>] [-FormatVersion <Int32>] [-AsJob] [-EnableTrafficAnalytics]
 -WorkspaceResourceId <String> -WorkspaceGUID <String> -WorkspaceLocation <String>
 [-TrafficAnalyticsInterval <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7d7da-108">SetFlowlogByNameWithTAByResource</span><span class="sxs-lookup"><span data-stu-id="7d7da-108">SetFlowlogByNameWithTAByResource</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>]
 [-RetentionInDays <Int32>] [-FormatType <String>] [-FormatVersion <Int32>] [-AsJob] [-EnableTrafficAnalytics]
 -Workspace <IOperationalInsightWorkspace> [-TrafficAnalyticsInterval <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d7da-109">SetFlowlogByNameWithTAByDetails</span><span class="sxs-lookup"><span data-stu-id="7d7da-109">SetFlowlogByNameWithTAByDetails</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>]
 [-RetentionInDays <Int32>] [-FormatType <String>] [-FormatVersion <Int32>] [-AsJob] [-EnableTrafficAnalytics]
 -WorkspaceResourceId <String> -WorkspaceGUID <String> -WorkspaceLocation <String>
 [-TrafficAnalyticsInterval <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7d7da-110">SetFlowlogByNameWithoutTA</span><span class="sxs-lookup"><span data-stu-id="7d7da-110">SetFlowlogByNameWithoutTA</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>]
 [-RetentionInDays <Int32>] [-FormatType <String>] [-FormatVersion <Int32>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d7da-111">SetFlowlogByLocationWithTAByResource</span><span class="sxs-lookup"><span data-stu-id="7d7da-111">SetFlowlogByLocationWithTAByResource</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -Location <String> -TargetResourceId <String> -EnableFlowLog <Boolean>
 -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-AsJob] [-EnableTrafficAnalytics] -Workspace <IOperationalInsightWorkspace>
 [-TrafficAnalyticsInterval <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7d7da-112">SetFlowlogByLocationWithTAByDetails</span><span class="sxs-lookup"><span data-stu-id="7d7da-112">SetFlowlogByLocationWithTAByDetails</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -Location <String> -TargetResourceId <String> -EnableFlowLog <Boolean>
 -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-AsJob] [-EnableTrafficAnalytics] -WorkspaceResourceId <String>
 -WorkspaceGUID <String> -WorkspaceLocation <String> [-TrafficAnalyticsInterval <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d7da-113">SetFlowlogByLocationWithoutTA</span><span class="sxs-lookup"><span data-stu-id="7d7da-113">SetFlowlogByLocationWithoutTA</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -Location <String> -TargetResourceId <String> -EnableFlowLog <Boolean>
 -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7d7da-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7d7da-114">DESCRIPTION</span></span>
<span data-ttu-id="7d7da-115">Die Set-AzNetworkWatcherConfigFlowLog konfiguriert die Flussprotokollierung für eine Zielressource.</span><span class="sxs-lookup"><span data-stu-id="7d7da-115">The Set-AzNetworkWatcherConfigFlowLog configures flow logging for a target resource.</span></span> <span data-ttu-id="7d7da-116">Zu den zu konfigurierenden Eigenschaften gehören: ob die Flussprotokollierung für die bereitgestellte Ressource aktiviert ist oder nicht, das konfigurierte Speicherkonto zum Senden von Protokollen, das Flussprotokollierungsformat und die Aufbewahrungsrichtlinie für die Protokolle.</span><span class="sxs-lookup"><span data-stu-id="7d7da-116">Properties to configure include: whether or not flow logging is enabled for the resource provided, the configured storage account to send logs, the flow logging format, and the retention policy for the logs.</span></span> <span data-ttu-id="7d7da-117">Derzeit werden Netzwerksicherheitsgruppen für die Flussprotokollierung unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7d7da-117">Currently Network Security Groups are supported for flow logging.</span></span> 

## <span data-ttu-id="7d7da-118">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="7d7da-118">EXAMPLES</span></span>

### <span data-ttu-id="7d7da-119">Beispiel 1: Konfigurieren der Flussprotokollierung für ein angegebenes NSG</span><span class="sxs-lookup"><span data-stu-id="7d7da-119">Example 1: Configure Flow Logging for a Specified NSG</span></span>
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

<span data-ttu-id="7d7da-120">In diesem Beispiel wird der Status der Flussprotokollierung für eine Netzwerksicherheitsgruppe konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="7d7da-120">In this example we configure flow logging status for a Network Security Group.</span></span> <span data-ttu-id="7d7da-121">In der Antwort sehen Sie, dass für das angegebene NSG die Flussprotokollierung aktiviert ist, das Standardformat und keine Aufbewahrungsrichtlinien festgelegt wurden.</span><span class="sxs-lookup"><span data-stu-id="7d7da-121">In the response, we see the specified NSG has flow logging enabled, default format, and no retention policy set.</span></span>

### <span data-ttu-id="7d7da-122">Beispiel 2: Konfigurieren der Flussprotokollierung für ein angegebenes NSG und Festlegen der Version der Flussprotokollierung auf 2.</span><span class="sxs-lookup"><span data-stu-id="7d7da-122">Example 2: Configure Flow Logging for a Specified NSG and set the version of flow logging to 2.</span></span>
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

<span data-ttu-id="7d7da-123">In diesem Beispiel wird die Flussprotokollierung für eine Netzwerksicherheitsgruppe (Network Security Group, NSG) mit angegebenen Protokollen der Version 2 konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="7d7da-123">In this example, we configure flow logging on a Network Security Group (NSG) with version 2 logs specified.</span></span> <span data-ttu-id="7d7da-124">In der Antwort sehen wir, dass für das angegebene NSG die Flussprotokollierung aktiviert ist, das Format festgelegt ist und keine Aufbewahrungsrichtlinie konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="7d7da-124">In the response, we see the specified NSG has flow logging enabled, the format is set, and there is no retention policy configured.</span></span> <span data-ttu-id="7d7da-125">Wenn die Region die angegebene Version nicht unterstützt, schreibt Network Watcher die unterstützte Standardversion in der Region.</span><span class="sxs-lookup"><span data-stu-id="7d7da-125">If the region does not support version you specified, Network Watcher will write the default supported version in the region.</span></span>

### <span data-ttu-id="7d7da-126">Beispiel 3: Konfigurieren der Flussprotokollierung und Datenverkehrsanalyse für ein angegebenes NSG</span><span class="sxs-lookup"><span data-stu-id="7d7da-126">Example 3: Configure Flow Logging and Traffic Analytics for a Specified NSG</span></span>
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

<span data-ttu-id="7d7da-127">In diesem Beispiel konfigurieren wir den Flussprotokollierungsstatus und die Datenverkehrsanalyse für eine Netzwerksicherheitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="7d7da-127">In this example we configure flow logging status and Traffic Analytics for a Network Security Group.</span></span> <span data-ttu-id="7d7da-128">In der Antwort sehen wir, dass für das angegebene NSG Die Flussprotokollierung und Datenverkehrsanalyse aktiviert ist, das Standardformat und keine Aufbewahrungsrichtlinien festgelegt wurden.</span><span class="sxs-lookup"><span data-stu-id="7d7da-128">In the response, we see the specified NSG has flow logging and Traffic Analytics enabled, default format, and no retention policy set.</span></span>

### <span data-ttu-id="7d7da-129">Beispiel 4: Deaktivieren der Datenverkehrsanalyse für ein angegebenes NSG mit konfigurierter Flussprotokollierung und Datenverkehrsanalyse</span><span class="sxs-lookup"><span data-stu-id="7d7da-129">Example 4: Disable Traffic Analytics for a Specified NSG with Flow Logging and Traffic Analytics configured</span></span>
```
PS C:\> $NW = Get-AzNetworkWatcher -ResourceGroupName NetworkWatcherRg -Name NetworkWatcher_westcentralus
PS C:\> $nsg = Get-AzNetworkSecurityGroup -ResourceGroupName NSGRG -Name appNSG
PS C:\> $storageId = "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123"
PS C:\> $workspace = Get-AzOperationalInsightsWorkspace -Name WorkspaceName -ResourceGroupName WorkspaceRg
PS C:\> Set-AzNetworkWatcherConfigFlowLog -NetworkWatcher $NW -TargetResourceId $nsg.Id -EnableFlowLog $true -StorageAccountId $storageID -EnableTrafficAnalytics -Workspace $workspace -TrafficAnalyticsInterval 60


PS C:\> Set-AzNetworkWatcherConfigFlowLog -NetworkWatcher $NW -TargetResourceId $nsg.Id -EnableFlowLog $true -StorageAccountId $storageID -EnableTrafficAnalytics:$false -Workspace $workspace

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
              "enabled": false,
              "workspaceId": "bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb",
              "workspaceRegion": "WorkspaceLocation",
              "workspaceResourceId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourcegroups/WorkspaceRg/providers/microsoft.operationalinsights/workspaces/WorkspaceName",
          "TrafficAnalyticsInterval": 60
            }
          }
```

<span data-ttu-id="7d7da-130">In diesem Beispiel deaktivieren wir die Datenverkehrsanalyse für eine Netzwerksicherheitsgruppe, für die die Flussprotokollierung und die Datenverkehrsanalyse zuvor konfiguriert wurden.</span><span class="sxs-lookup"><span data-stu-id="7d7da-130">In this example we disable Traffic Analytics for a Network Security Group which has flow logging and Traffic Analytics configured earlier.</span></span> <span data-ttu-id="7d7da-131">In der Antwort sehen wir, dass die Flussprotokollierung für das angegebene NSG aktiviert ist, die Datenverkehrsanalyse jedoch deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="7d7da-131">In the response, we see the specified NSG has flow logging enabled but Traffic Analytics disabled.</span></span>

## <span data-ttu-id="7d7da-132">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7d7da-132">PARAMETERS</span></span>

### <span data-ttu-id="7d7da-133">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7d7da-133">-AsJob</span></span>
<span data-ttu-id="7d7da-134">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="7d7da-134">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7d7da-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d7da-135">-DefaultProfile</span></span>
<span data-ttu-id="7d7da-136">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7d7da-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7d7da-137">-EnableFlowLog</span><span class="sxs-lookup"><span data-stu-id="7d7da-137">-EnableFlowLog</span></span>
<span data-ttu-id="7d7da-138">Zum Aktivieren/Deaktivieren der Flussprotokollierung kennzeichnen.</span><span class="sxs-lookup"><span data-stu-id="7d7da-138">Flag to enable/disable flow logging.</span></span>

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

### <span data-ttu-id="7d7da-139">-EnableRetention</span><span class="sxs-lookup"><span data-stu-id="7d7da-139">-EnableRetention</span></span>
<span data-ttu-id="7d7da-140">Kennzeichnen, um die Aufbewahrung zu aktivieren/zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="7d7da-140">Flag to enable/disable retention.</span></span>

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

### <span data-ttu-id="7d7da-141">-EnableTrafficAnalytics</span><span class="sxs-lookup"><span data-stu-id="7d7da-141">-EnableTrafficAnalytics</span></span>
<span data-ttu-id="7d7da-142">Zum Aktivieren/Deaktivieren der Aufbewahrung kennzeichnen.</span><span class="sxs-lookup"><span data-stu-id="7d7da-142">Flag to enable/disable retention.</span></span>

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

### <span data-ttu-id="7d7da-143">-FormatType</span><span class="sxs-lookup"><span data-stu-id="7d7da-143">-FormatType</span></span>
<span data-ttu-id="7d7da-144">Typ des Flussprotokollformats.</span><span class="sxs-lookup"><span data-stu-id="7d7da-144">Type of flow log format.</span></span>

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

### <span data-ttu-id="7d7da-145">-FormatVersion</span><span class="sxs-lookup"><span data-stu-id="7d7da-145">-FormatVersion</span></span>
<span data-ttu-id="7d7da-146">Version des Flussprotokollformats.</span><span class="sxs-lookup"><span data-stu-id="7d7da-146">Version of flow log format.</span></span>

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

### <span data-ttu-id="7d7da-147">-Location</span><span class="sxs-lookup"><span data-stu-id="7d7da-147">-Location</span></span>
<span data-ttu-id="7d7da-148">Position der Netzwerk-Watcher.</span><span class="sxs-lookup"><span data-stu-id="7d7da-148">Location of the network watcher.</span></span>

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

### <span data-ttu-id="7d7da-149">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7d7da-149">-NetworkWatcher</span></span>
<span data-ttu-id="7d7da-150">Die Netzwerk-Watcher-Ressource.</span><span class="sxs-lookup"><span data-stu-id="7d7da-150">The network watcher resource.</span></span>

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

### <span data-ttu-id="7d7da-151">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="7d7da-151">-NetworkWatcherName</span></span>
<span data-ttu-id="7d7da-152">Der Name der Netzwerk-Watcher.</span><span class="sxs-lookup"><span data-stu-id="7d7da-152">The name of network watcher.</span></span>

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

### <span data-ttu-id="7d7da-153">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d7da-153">-ResourceGroupName</span></span>
<span data-ttu-id="7d7da-154">Der Name der Ressourcengruppe "Netzwerk-Watcher".</span><span class="sxs-lookup"><span data-stu-id="7d7da-154">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="7d7da-155">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="7d7da-155">-RetentionInDays</span></span>
<span data-ttu-id="7d7da-156">Die Anzahl der Tage, die die Flussprotokolldatensätze beibehalten werden müssen.</span><span class="sxs-lookup"><span data-stu-id="7d7da-156">Number of days to retain flow log records.</span></span>

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

### <span data-ttu-id="7d7da-157">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="7d7da-157">-StorageAccountId</span></span>
<span data-ttu-id="7d7da-158">DIE ID des Speicherkontos, das zum Speichern des Flussprotokolls verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7d7da-158">ID of the storage account which is used to store the flow log.</span></span>

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

### <span data-ttu-id="7d7da-159">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="7d7da-159">-TargetResourceId</span></span>
<span data-ttu-id="7d7da-160">Die Zielressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="7d7da-160">The target resource ID.</span></span>

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

### <span data-ttu-id="7d7da-161">-TrafficAnalyticsInterval</span><span class="sxs-lookup"><span data-stu-id="7d7da-161">-TrafficAnalyticsInterval</span></span>
<span data-ttu-id="7d7da-162">Ruft das Intervall (in Minuten) ab oder legt es fest, welches entscheiden würde, wie häufig der Ta-Dienst Flussanalysen erstellen soll.</span><span class="sxs-lookup"><span data-stu-id="7d7da-162">Gets or sets the interval (in minutes) which would decide how frequently TA service should do flow analytics.</span></span>

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

### <span data-ttu-id="7d7da-163">-Workspace</span><span class="sxs-lookup"><span data-stu-id="7d7da-163">-Workspace</span></span>
<span data-ttu-id="7d7da-164">Das WS-Objekt, das zum Speichern der Datenverkehrsanalysedaten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7d7da-164">The WS object which is used to store the traffic analytics data.</span></span>

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

### <span data-ttu-id="7d7da-165">-WorkspaceGUID</span><span class="sxs-lookup"><span data-stu-id="7d7da-165">-WorkspaceGUID</span></span>
<span data-ttu-id="7d7da-166">GUID der WS, die zum Speichern der Datenverkehrsanalysedaten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7d7da-166">GUID of the WS which is used to store the traffic analytics data.</span></span>

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

### <span data-ttu-id="7d7da-167">-WorkspaceLocation</span><span class="sxs-lookup"><span data-stu-id="7d7da-167">-WorkspaceLocation</span></span>
<span data-ttu-id="7d7da-168">Azure Region der WS, die zum Speichern der Datenverkehrsanalysedaten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7d7da-168">Azure Region of the WS which is used to store the traffic analytics data.</span></span>

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

### <span data-ttu-id="7d7da-169">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="7d7da-169">-WorkspaceResourceId</span></span>
<span data-ttu-id="7d7da-170">Abonnement der WS, die zum Speichern der Datenverkehrsanalysedaten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7d7da-170">Subscription of the WS which is used to store the traffic analytics data.</span></span>

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

### <span data-ttu-id="7d7da-171">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7d7da-171">-Confirm</span></span>
<span data-ttu-id="7d7da-172">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7d7da-172">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7d7da-173">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="7d7da-173">-WhatIf</span></span>
<span data-ttu-id="7d7da-174">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7d7da-174">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7d7da-175">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7d7da-175">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7d7da-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d7da-176">CommonParameters</span></span>
<span data-ttu-id="7d7da-177">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d7da-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d7da-178">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d7da-178">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d7da-179">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="7d7da-179">INPUTS</span></span>

### <span data-ttu-id="7d7da-180">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7d7da-180">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="7d7da-181">System.String</span><span class="sxs-lookup"><span data-stu-id="7d7da-181">System.String</span></span>

### <span data-ttu-id="7d7da-182">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7d7da-182">System.Boolean</span></span>

### <span data-ttu-id="7d7da-183">System.Int32</span><span class="sxs-lookup"><span data-stu-id="7d7da-183">System.Int32</span></span>

### <span data-ttu-id="7d7da-184">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="7d7da-184">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="7d7da-185">Microsoft.Azure.Management.Internal.Network.Common.IOperationalInsightWorkspace</span><span class="sxs-lookup"><span data-stu-id="7d7da-185">Microsoft.Azure.Management.Internal.Network.Common.IOperationalInsightWorkspace</span></span>

## <span data-ttu-id="7d7da-186">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="7d7da-186">OUTPUTS</span></span>

### <span data-ttu-id="7d7da-187">Microsoft.Azure.Commands.Network.Models.PSFlowLog</span><span class="sxs-lookup"><span data-stu-id="7d7da-187">Microsoft.Azure.Commands.Network.Models.PSFlowLog</span></span>

## <span data-ttu-id="7d7da-188">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="7d7da-188">NOTES</span></span>
<span data-ttu-id="7d7da-189">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, network, networking, watcher, flow, logs, flowlog, logging</span><span class="sxs-lookup"><span data-stu-id="7d7da-189">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, flow, logs, flowlog, logging</span></span>

## <span data-ttu-id="7d7da-190">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="7d7da-190">RELATED LINKS</span></span>

[<span data-ttu-id="7d7da-191">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7d7da-191">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="7d7da-192">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7d7da-192">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="7d7da-193">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7d7da-193">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="7d7da-194">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="7d7da-194">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="7d7da-195">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="7d7da-195">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="7d7da-196">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="7d7da-196">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="7d7da-197">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="7d7da-197">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="7d7da-198">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7d7da-198">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="7d7da-199">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="7d7da-199">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="7d7da-200">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7d7da-200">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="7d7da-201">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7d7da-201">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="7d7da-202">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7d7da-202">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="7d7da-203">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="7d7da-203">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="7d7da-204">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="7d7da-204">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="7d7da-205">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="7d7da-205">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="7d7da-206">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="7d7da-206">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="7d7da-207">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="7d7da-207">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="7d7da-208">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="7d7da-208">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="7d7da-209">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="7d7da-209">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="7d7da-210">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="7d7da-210">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="7d7da-211">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="7d7da-211">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="7d7da-212">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="7d7da-212">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="7d7da-213">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="7d7da-213">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="7d7da-214">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="7d7da-214">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="7d7da-215">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="7d7da-215">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="7d7da-216">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="7d7da-216">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="7d7da-217">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="7d7da-217">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)
