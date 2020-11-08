---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkwatcherconfigflowlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkWatcherConfigFlowLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkWatcherConfigFlowLog.md
ms.openlocfilehash: 7212c3cbfad4c3f6cd3c3dfee778645156da288c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94003307"
---
# <span data-ttu-id="b050f-101">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="b050f-101">Set-AzNetworkWatcherConfigFlowLog</span></span>

## <span data-ttu-id="b050f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b050f-102">SYNOPSIS</span></span>
<span data-ttu-id="b050f-103">Konfiguriert die Fluss Protokollierung für eine Zielressource.</span><span class="sxs-lookup"><span data-stu-id="b050f-103">Configures flow logging for a target resource.</span></span>

## <span data-ttu-id="b050f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b050f-104">SYNTAX</span></span>

### <span data-ttu-id="b050f-105">SetFlowlogByResourceWithoutTA (Standard)</span><span class="sxs-lookup"><span data-stu-id="b050f-105">SetFlowlogByResourceWithoutTA (Default)</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>]
 [-FormatType <String>] [-FormatVersion <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b050f-106">SetFlowlogByResourceWithTAByResource</span><span class="sxs-lookup"><span data-stu-id="b050f-106">SetFlowlogByResourceWithTAByResource</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>]
 [-FormatType <String>] [-FormatVersion <Int32>] [-AsJob] [-EnableTrafficAnalytics]
 -Workspace <IOperationalInsightWorkspace> [-TrafficAnalyticsInterval <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b050f-107">SetFlowlogByResourceWithTAByDetails</span><span class="sxs-lookup"><span data-stu-id="b050f-107">SetFlowlogByResourceWithTAByDetails</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>]
 [-FormatType <String>] [-FormatVersion <Int32>] [-AsJob] [-EnableTrafficAnalytics]
 -WorkspaceResourceId <String> -WorkspaceGUID <String> -WorkspaceLocation <String>
 [-TrafficAnalyticsInterval <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b050f-108">SetFlowlogByNameWithTAByResource</span><span class="sxs-lookup"><span data-stu-id="b050f-108">SetFlowlogByNameWithTAByResource</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>]
 [-RetentionInDays <Int32>] [-FormatType <String>] [-FormatVersion <Int32>] [-AsJob] [-EnableTrafficAnalytics]
 -Workspace <IOperationalInsightWorkspace> [-TrafficAnalyticsInterval <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b050f-109">SetFlowlogByNameWithTAByDetails</span><span class="sxs-lookup"><span data-stu-id="b050f-109">SetFlowlogByNameWithTAByDetails</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>]
 [-RetentionInDays <Int32>] [-FormatType <String>] [-FormatVersion <Int32>] [-AsJob] [-EnableTrafficAnalytics]
 -WorkspaceResourceId <String> -WorkspaceGUID <String> -WorkspaceLocation <String>
 [-TrafficAnalyticsInterval <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b050f-110">SetFlowlogByNameWithoutTA</span><span class="sxs-lookup"><span data-stu-id="b050f-110">SetFlowlogByNameWithoutTA</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>]
 [-RetentionInDays <Int32>] [-FormatType <String>] [-FormatVersion <Int32>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b050f-111">SetFlowlogByLocationWithTAByResource</span><span class="sxs-lookup"><span data-stu-id="b050f-111">SetFlowlogByLocationWithTAByResource</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -Location <String> -TargetResourceId <String> -EnableFlowLog <Boolean>
 -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-AsJob] [-EnableTrafficAnalytics] -Workspace <IOperationalInsightWorkspace>
 [-TrafficAnalyticsInterval <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b050f-112">SetFlowlogByLocationWithTAByDetails</span><span class="sxs-lookup"><span data-stu-id="b050f-112">SetFlowlogByLocationWithTAByDetails</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -Location <String> -TargetResourceId <String> -EnableFlowLog <Boolean>
 -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-AsJob] [-EnableTrafficAnalytics] -WorkspaceResourceId <String>
 -WorkspaceGUID <String> -WorkspaceLocation <String> [-TrafficAnalyticsInterval <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b050f-113">SetFlowlogByLocationWithoutTA</span><span class="sxs-lookup"><span data-stu-id="b050f-113">SetFlowlogByLocationWithoutTA</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -Location <String> -TargetResourceId <String> -EnableFlowLog <Boolean>
 -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b050f-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b050f-114">DESCRIPTION</span></span>
<span data-ttu-id="b050f-115">Die Set-AzNetworkWatcherConfigFlowLog konfiguriert die Fluss Protokollierung für eine Zielressource.</span><span class="sxs-lookup"><span data-stu-id="b050f-115">The Set-AzNetworkWatcherConfigFlowLog configures flow logging for a target resource.</span></span> <span data-ttu-id="b050f-116">Zu konfigurierende Eigenschaften: gibt an, ob die Fluss Protokollierung für die bereitgestellte Ressource aktiviert ist, das konfigurierte Speicherkonto zum Senden von Protokollen, das Fluss Protokollierungsformat und die Aufbewahrungsrichtlinie für die Protokolle.</span><span class="sxs-lookup"><span data-stu-id="b050f-116">Properties to configure include: whether or not flow logging is enabled for the resource provided, the configured storage account to send logs, the flow logging format, and the retention policy for the logs.</span></span> <span data-ttu-id="b050f-117">Zurzeit werden Netzwerk Sicherheitsgruppen für die Fluss Protokollierung unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b050f-117">Currently Network Security Groups are supported for flow logging.</span></span> 

## <span data-ttu-id="b050f-118">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b050f-118">EXAMPLES</span></span>

### <span data-ttu-id="b050f-119">Beispiel 1: Konfigurieren der Fluss Protokollierung für ein angegebenes NSG</span><span class="sxs-lookup"><span data-stu-id="b050f-119">Example 1: Configure Flow Logging for a Specified NSG</span></span>
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

<span data-ttu-id="b050f-120">In diesem Beispiel wird der Fluss Protokollierungsstatus für eine Netzwerksicherheitsgruppe konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="b050f-120">In this example we configure flow logging status for a Network Security Group.</span></span> <span data-ttu-id="b050f-121">In der Antwort sehen wir die angegebene NSG hat die Fluss Protokollierung aktiviert, das Standardformat und keine Aufbewahrungsrichtlinien festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b050f-121">In the response, we see the specified NSG has flow logging enabled, default format, and no retention policy set.</span></span>

### <span data-ttu-id="b050f-122">Beispiel 2: Konfigurieren Sie die Fluss Protokollierung für einen angegebenen NSG, und legen Sie die Version der Fluss Protokollierung auf 2 fest.</span><span class="sxs-lookup"><span data-stu-id="b050f-122">Example 2: Configure Flow Logging for a Specified NSG and set the version of flow logging to 2.</span></span>
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

<span data-ttu-id="b050f-123">In diesem Beispiel wird die Fluss Protokollierung in einer Network Security Group (NSG) mit den angegebenen Protokollen der Version 2 konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="b050f-123">In this example, we configure flow logging on a Network Security Group (NSG) with version 2 logs specified.</span></span> <span data-ttu-id="b050f-124">In der Antwort sehen wir den angegebenen NSG ist die Fluss Protokollierung aktiviert, das Format ist festgelegt, und es ist keine Aufbewahrungsrichtlinie konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="b050f-124">In the response, we see the specified NSG has flow logging enabled, the format is set, and there is no retention policy configured.</span></span> <span data-ttu-id="b050f-125">Wenn die von Ihnen angegebene Version von der Region nicht unterstützt wird, schreibt Network Watcher die standardmäßig unterstützte Version in der Region.</span><span class="sxs-lookup"><span data-stu-id="b050f-125">If the region does not support version you specified, Network Watcher will write the default supported version in the region.</span></span>

### <span data-ttu-id="b050f-126">Beispiel 3: Konfigurieren der Fluss Protokollierung und der Datenverkehrsanalyse für ein angegebenes NSG</span><span class="sxs-lookup"><span data-stu-id="b050f-126">Example 3: Configure Flow Logging and Traffic Analytics for a Specified NSG</span></span>
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

<span data-ttu-id="b050f-127">In diesem Beispiel konfigurieren wir den Fluss Protokollierungsstatus und die Datenverkehrsanalyse für eine Netzwerksicherheitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="b050f-127">In this example we configure flow logging status and Traffic Analytics for a Network Security Group.</span></span> <span data-ttu-id="b050f-128">In der Antwort sehen wir, dass die angegebene NSG-Funktion Datenflussprotokollierung und Datenverkehrsanalyse aktiviert, Standardformat und keine Aufbewahrungsrichtlinie festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="b050f-128">In the response, we see the specified NSG has flow logging and Traffic Analytics enabled, default format, and no retention policy set.</span></span>

### <span data-ttu-id="b050f-129">Beispiel 4: Deaktivieren der Datenverkehrsanalyse für einen angegebenen NSG mit konfigurierter Fluss Protokollierung und Datenverkehrsanalyse</span><span class="sxs-lookup"><span data-stu-id="b050f-129">Example 4: Disable Traffic Analytics for a Specified NSG with Flow Logging and Traffic Analytics configured</span></span>
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

<span data-ttu-id="b050f-130">In diesem Beispiel wird die Datenverkehrsanalyse für eine Netzwerksicherheitsgruppe deaktiviert, bei der die Fluss Protokollierung und die Datenverkehrsanalyse zuvor konfiguriert wurden.</span><span class="sxs-lookup"><span data-stu-id="b050f-130">In this example we disable Traffic Analytics for a Network Security Group which has flow logging and Traffic Analytics configured earlier.</span></span> <span data-ttu-id="b050f-131">In der Antwort sehen wir den angegebenen NSG ist die Fluss Protokollierung aktiviert, aber die Datenverkehrsanalyse ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="b050f-131">In the response, we see the specified NSG has flow logging enabled but Traffic Analytics disabled.</span></span>

## <span data-ttu-id="b050f-132">Parameter</span><span class="sxs-lookup"><span data-stu-id="b050f-132">PARAMETERS</span></span>

### <span data-ttu-id="b050f-133">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b050f-133">-AsJob</span></span>
<span data-ttu-id="b050f-134">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="b050f-134">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b050f-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b050f-135">-DefaultProfile</span></span>
<span data-ttu-id="b050f-136">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b050f-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b050f-137">-EnableFlowLog</span><span class="sxs-lookup"><span data-stu-id="b050f-137">-EnableFlowLog</span></span>
<span data-ttu-id="b050f-138">Kennzeichnen, um die Fluss Protokollierung zu aktivieren/deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="b050f-138">Flag to enable/disable flow logging.</span></span>

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

### <span data-ttu-id="b050f-139">-EnableRetention</span><span class="sxs-lookup"><span data-stu-id="b050f-139">-EnableRetention</span></span>
<span data-ttu-id="b050f-140">Flag zum Aktivieren/Deaktivieren der Aufbewahrung.</span><span class="sxs-lookup"><span data-stu-id="b050f-140">Flag to enable/disable retention.</span></span>

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

### <span data-ttu-id="b050f-141">-EnableTrafficAnalytics</span><span class="sxs-lookup"><span data-stu-id="b050f-141">-EnableTrafficAnalytics</span></span>
<span data-ttu-id="b050f-142">Flag zum Aktivieren/Deaktivieren der Aufbewahrung.</span><span class="sxs-lookup"><span data-stu-id="b050f-142">Flag to enable/disable retention.</span></span>

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

### <span data-ttu-id="b050f-143">-Formattyp</span><span class="sxs-lookup"><span data-stu-id="b050f-143">-FormatType</span></span>
<span data-ttu-id="b050f-144">Der Typ des Fluss Protokollformats.</span><span class="sxs-lookup"><span data-stu-id="b050f-144">Type of flow log format.</span></span>

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

### <span data-ttu-id="b050f-145">-FormatVersion</span><span class="sxs-lookup"><span data-stu-id="b050f-145">-FormatVersion</span></span>
<span data-ttu-id="b050f-146">Version des Flow Log-Formats.</span><span class="sxs-lookup"><span data-stu-id="b050f-146">Version of flow log format.</span></span>

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

### <span data-ttu-id="b050f-147">-Standort</span><span class="sxs-lookup"><span data-stu-id="b050f-147">-Location</span></span>
<span data-ttu-id="b050f-148">Der Speicherort des Netzwerkmonitors.</span><span class="sxs-lookup"><span data-stu-id="b050f-148">Location of the network watcher.</span></span>

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

### <span data-ttu-id="b050f-149">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b050f-149">-NetworkWatcher</span></span>
<span data-ttu-id="b050f-150">Die Netzwerk Überwachungsressource.</span><span class="sxs-lookup"><span data-stu-id="b050f-150">The network watcher resource.</span></span>

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

### <span data-ttu-id="b050f-151">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="b050f-151">-NetworkWatcherName</span></span>
<span data-ttu-id="b050f-152">Der Name des Netzwerkmonitors.</span><span class="sxs-lookup"><span data-stu-id="b050f-152">The name of network watcher.</span></span>

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

### <span data-ttu-id="b050f-153">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b050f-153">-ResourceGroupName</span></span>
<span data-ttu-id="b050f-154">Der Name der Netzwerk Überwachungsressourcen Gruppe.</span><span class="sxs-lookup"><span data-stu-id="b050f-154">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="b050f-155">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="b050f-155">-RetentionInDays</span></span>
<span data-ttu-id="b050f-156">Die Anzahl der Tage, an denen Fluss Protokolldatensätze beibehalten werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b050f-156">Number of days to retain flow log records.</span></span>

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

### <span data-ttu-id="b050f-157">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="b050f-157">-StorageAccountId</span></span>
<span data-ttu-id="b050f-158">Die ID des speicherkontos, das zum Speichern des Fluss Protokolls verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b050f-158">ID of the storage account which is used to store the flow log.</span></span>

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

### <span data-ttu-id="b050f-159">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="b050f-159">-TargetResourceId</span></span>
<span data-ttu-id="b050f-160">Die Ziel Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="b050f-160">The target resource ID.</span></span>

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

### <span data-ttu-id="b050f-161">-TrafficAnalyticsInterval</span><span class="sxs-lookup"><span data-stu-id="b050f-161">-TrafficAnalyticsInterval</span></span>
<span data-ttu-id="b050f-162">Ruft das Intervall (in Minuten) ab, das entscheiden würde, wie häufig der TA-Dienst Flussanalyse durchführen soll, oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="b050f-162">Gets or sets the interval (in minutes) which would decide how frequently TA service should do flow analytics.</span></span>

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

### <span data-ttu-id="b050f-163">– Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="b050f-163">-Workspace</span></span>
<span data-ttu-id="b050f-164">Das WS-Objekt, das zum Speichern der Daten zur Datenverkehrsanalyse verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b050f-164">The WS object which is used to store the traffic analytics data.</span></span>

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

### <span data-ttu-id="b050f-165">-WorkspaceGUID</span><span class="sxs-lookup"><span data-stu-id="b050f-165">-WorkspaceGUID</span></span>
<span data-ttu-id="b050f-166">Die GUID des WS, die zum Speichern der Daten zur Datenverkehrsanalyse verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b050f-166">GUID of the WS which is used to store the traffic analytics data.</span></span>

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

### <span data-ttu-id="b050f-167">-WorkspaceLocation</span><span class="sxs-lookup"><span data-stu-id="b050f-167">-WorkspaceLocation</span></span>
<span data-ttu-id="b050f-168">Der Azure-Bereich des WS, der zum Speichern der Daten für die Datenverkehrsanalyse verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b050f-168">Azure Region of the WS which is used to store the traffic analytics data.</span></span>

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

### <span data-ttu-id="b050f-169">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="b050f-169">-WorkspaceResourceId</span></span>
<span data-ttu-id="b050f-170">Das Abonnement des WS, das zum Speichern der Daten zur Datenverkehrsanalyse verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b050f-170">Subscription of the WS which is used to store the traffic analytics data.</span></span>

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

### <span data-ttu-id="b050f-171">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b050f-171">-Confirm</span></span>
<span data-ttu-id="b050f-172">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b050f-172">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b050f-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b050f-173">-WhatIf</span></span>
<span data-ttu-id="b050f-174">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b050f-174">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b050f-175">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b050f-175">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b050f-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b050f-176">CommonParameters</span></span>
<span data-ttu-id="b050f-177">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b050f-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b050f-178">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b050f-178">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b050f-179">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b050f-179">INPUTS</span></span>

### <span data-ttu-id="b050f-180">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b050f-180">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="b050f-181">System. String</span><span class="sxs-lookup"><span data-stu-id="b050f-181">System.String</span></span>

### <span data-ttu-id="b050f-182">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b050f-182">System.Boolean</span></span>

### <span data-ttu-id="b050f-183">System. Int32</span><span class="sxs-lookup"><span data-stu-id="b050f-183">System.Int32</span></span>

### <span data-ttu-id="b050f-184">System. Nullable ' 1 [[System. Int32, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="b050f-184">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="b050f-185">Microsoft. Azure. Management. Internal. Network. Common. IOperationalInsightWorkspace</span><span class="sxs-lookup"><span data-stu-id="b050f-185">Microsoft.Azure.Management.Internal.Network.Common.IOperationalInsightWorkspace</span></span>

## <span data-ttu-id="b050f-186">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b050f-186">OUTPUTS</span></span>

### <span data-ttu-id="b050f-187">Microsoft. Azure. Commands. Network. Models. PSFlowLog</span><span class="sxs-lookup"><span data-stu-id="b050f-187">Microsoft.Azure.Commands.Network.Models.PSFlowLog</span></span>

## <span data-ttu-id="b050f-188">Notizen</span><span class="sxs-lookup"><span data-stu-id="b050f-188">NOTES</span></span>
<span data-ttu-id="b050f-189">Schlüsselwörter: Azure, azurerm, arm, Resource, Verwaltung, Manager, Netzwerk, Netzwerk, Watcher, Fluss, Protokolle, flowlog, Protokollierung</span><span class="sxs-lookup"><span data-stu-id="b050f-189">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, flow, logs, flowlog, logging</span></span>

## <span data-ttu-id="b050f-190">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b050f-190">RELATED LINKS</span></span>

[<span data-ttu-id="b050f-191">Neu – AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b050f-191">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="b050f-192">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b050f-192">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="b050f-193">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b050f-193">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="b050f-194">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="b050f-194">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="b050f-195">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="b050f-195">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="b050f-196">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="b050f-196">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="b050f-197">Anfang-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="b050f-197">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="b050f-198">Neu – AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b050f-198">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="b050f-199">Neu – AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="b050f-199">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="b050f-200">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b050f-200">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="b050f-201">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b050f-201">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="b050f-202">Stopp-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b050f-202">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="b050f-203">Neu – AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="b050f-203">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="b050f-204">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="b050f-204">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="b050f-205">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="b050f-205">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="b050f-206">Stopp-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b050f-206">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="b050f-207">Anfang-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b050f-207">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="b050f-208">Satz-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b050f-208">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="b050f-209">Satz-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="b050f-209">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="b050f-210">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b050f-210">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="b050f-211">Neu – AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b050f-211">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="b050f-212">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="b050f-212">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="b050f-213">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="b050f-213">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="b050f-214">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="b050f-214">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="b050f-215">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="b050f-215">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="b050f-216">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="b050f-216">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="b050f-217">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b050f-217">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
