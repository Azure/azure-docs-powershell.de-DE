---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/new-azkustodataconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoDataConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoDataConnection.md
ms.openlocfilehash: ab58d679e9fc3ad62baeded8622b81a0cb8b2f95
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100170441"
---
# <span data-ttu-id="2d411-101">New-AzKustoDataConnection</span><span class="sxs-lookup"><span data-stu-id="2d411-101">New-AzKustoDataConnection</span></span>

## <span data-ttu-id="2d411-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2d411-102">SYNOPSIS</span></span>
<span data-ttu-id="2d411-103">Erstellt oder aktualisiert eine Datenverbindung.</span><span class="sxs-lookup"><span data-stu-id="2d411-103">Creates or updates a data connection.</span></span>

## <span data-ttu-id="2d411-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2d411-104">SYNTAX</span></span>

### <span data-ttu-id="2d411-105">CreateExpandedEventHub (Standard)</span><span class="sxs-lookup"><span data-stu-id="2d411-105">CreateExpandedEventHub (Default)</span></span>
```
New-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -EventHubResourceId <String> -Kind <Kind>
 -Location <String> [-SubscriptionId <String>] [-Compression <Compression>]
 [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>] [-MappingRuleName <String>]
 [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="2d411-106">CreateExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="2d411-106">CreateExpandedEventGrid</span></span>
```
New-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -EventHubResourceId <String> -Kind <Kind>
 -Location <String> -StorageAccountResourceId <String> [-SubscriptionId <String>]
 [-DataFormat <EventGridDataFormat>] [-MappingRuleName <String>] [-TableName <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="2d411-107">CreateExpandedIotHub</span><span class="sxs-lookup"><span data-stu-id="2d411-107">CreateExpandedIotHub</span></span>
```
New-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -IotHubResourceId <String> -Kind <Kind>
 -Location <String> -SharedAccessPolicyName <String> [-SubscriptionId <String>]
 [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>] [-MappingRuleName <String>]
 [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="2d411-108">UpdateExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="2d411-108">UpdateExpandedEventGrid</span></span>
```
New-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -Kind <Kind> -Location <String>
 [-SubscriptionId <String>] [-BlobStorageEventType <BlobStorageEventType>] [-DataFormat <EventGridDataFormat>]
 [-IgnoreFirstRecord] [-MappingRuleName <String>] [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="2d411-109">UpdateViaIdentityExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="2d411-109">UpdateViaIdentityExpandedEventGrid</span></span>
```
New-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -Kind <Kind> -Location <String>
 [-SubscriptionId <String>] [-BlobStorageEventType <BlobStorageEventType>] [-DataFormat <EventGridDataFormat>]
 [-IgnoreFirstRecord] [-MappingRuleName <String>] [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="2d411-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2d411-110">DESCRIPTION</span></span>
<span data-ttu-id="2d411-111">Erstellt oder aktualisiert eine Datenverbindung.</span><span class="sxs-lookup"><span data-stu-id="2d411-111">Creates or updates a data connection.</span></span>

## <span data-ttu-id="2d411-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2d411-112">EXAMPLES</span></span>

### <span data-ttu-id="2d411-113">Beispiel 1: Erstellen einer neuen EventHub-Datenverbindung</span><span class="sxs-lookup"><span data-stu-id="2d411-113">Example 1: Create a new EventHub data connection</span></span>
```powershell
PS C:\> New-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myeventhubdc" -Location="East US" -Kind "EventHub" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -DataFormat "JSON" -ConsumerGroup '$Default' -Compression "None" -TableName "Events" -MappingRuleName "EventsMapping"

Kind     Location Name                                             Type
----     -------- ----                                             ----
EventHub East US  testnewkustocluster/mykustodatabase/myeventhubdc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="2d411-114">Mit dem oben angegebenen Befehl wird eine neue EreignisHub-Datenverbindung namens "myeventhubdc" für die Datenbank "mykustodatabase" im Cluster "testnewkustocluster" erstellt.</span><span class="sxs-lookup"><span data-stu-id="2d411-114">The above command creates a new EventHub data connection named "myeventhubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="2d411-115">Beispiel 2: Erstellen einer neuen EventGrid-Datenverbindung</span><span class="sxs-lookup"><span data-stu-id="2d411-115">Example 2: Create a new EventGrid data connection</span></span>
```powershell
PS C:\> New-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myeventgriddc" -Location="East US" -Kind "EventGrid" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -StorageAccountResourceId $storageAccountResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Storage/storageAccounts/mystorage" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "EventsMapping" -IgnoreFirstRecord "false" -BlobStorageEventType "Microsoft.Storage.BlobRenamed"

Kind      Location Name                                              Type
----      -------- ----                                              ----
EventGrid East US  testnewkustocluster/mykustodatabase/myeventgriddc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="2d411-116">Der obige Befehl erstellt eine neue EventGrid-Datenverbindung mit dem Namen "myeventgriddc" für die Datenbank "mykustodatabase" im Cluster "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="2d411-116">The above command creates a new EventGrid data connection named "myeventgriddc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="2d411-117">Beispiel 3: Erstellen einer neuen IotHub-Datenverbindung</span><span class="sxs-lookup"><span data-stu-id="2d411-117">Example 3: Create a new IotHub data connection</span></span>
```powershell
PS C:\> New-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myiothubdc" -Location="East US" -Kind "IotHub" -IotHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Devices/IotHubs/myiothub" -SharedAccessPolicyName "myiothubpolicy" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "EventsMapping"

Kind      Location Name                                        Type
----      -------- ----                                        ----
IotHub East US  testnewkustocluster/mykustodatabase/myiothubdc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="2d411-118">Der obige Befehl erstellt eine neue IotHub-Datenverbindung namens "myiothubdc" für die Datenbank "mykustodatabase" im Cluster "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="2d411-118">The above command creates a new IotHub data connection named "myiothubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

## <span data-ttu-id="2d411-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2d411-119">PARAMETERS</span></span>

### <span data-ttu-id="2d411-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2d411-120">-AsJob</span></span>
<span data-ttu-id="2d411-121">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="2d411-121">Run the command as a job</span></span>

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

### <span data-ttu-id="2d411-122">-BlobStorageEventType</span><span class="sxs-lookup"><span data-stu-id="2d411-122">-BlobStorageEventType</span></span>
<span data-ttu-id="2d411-123">Der Name des zu verarbeitende BLOB-Speicherereignistyps.</span><span class="sxs-lookup"><span data-stu-id="2d411-123">The name of blob storage event type to process.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.BlobStorageEventType
Parameter Sets: UpdateExpandedEventGrid, UpdateViaIdentityExpandedEventGrid
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d411-124">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="2d411-124">-ClusterName</span></span>
<span data-ttu-id="2d411-125">Der Name des Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="2d411-125">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d411-126">-Compression</span><span class="sxs-lookup"><span data-stu-id="2d411-126">-Compression</span></span>
<span data-ttu-id="2d411-127">Der Komprimierungstyp für Ereignishubnachrichten.</span><span class="sxs-lookup"><span data-stu-id="2d411-127">The event hub messages compression type.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.Compression
Parameter Sets: CreateExpandedEventHub
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d411-128">-ConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="2d411-128">-ConsumerGroup</span></span>
<span data-ttu-id="2d411-129">Die Consumergruppe "Ereignis/iot-Hub".</span><span class="sxs-lookup"><span data-stu-id="2d411-129">The event/iot hub consumer group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d411-130">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="2d411-130">-DatabaseName</span></span>
<span data-ttu-id="2d411-131">Der Name der Datenbank im Cluster "Kusto".</span><span class="sxs-lookup"><span data-stu-id="2d411-131">The name of the database in the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d411-132">-DataFormat</span><span class="sxs-lookup"><span data-stu-id="2d411-132">-DataFormat</span></span>
<span data-ttu-id="2d411-133">Das Datenformat der Nachricht.</span><span class="sxs-lookup"><span data-stu-id="2d411-133">The data format of the message.</span></span>
<span data-ttu-id="2d411-134">Optional kann jeder Nachricht das Datenformat hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="2d411-134">Optionally the data format can be added to each message.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.EventGridDataFormat
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d411-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d411-135">-DefaultProfile</span></span>
<span data-ttu-id="2d411-136">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2d411-136">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d411-137">-EventHubResourceId</span><span class="sxs-lookup"><span data-stu-id="2d411-137">-EventHubResourceId</span></span>
<span data-ttu-id="2d411-138">Die Ressourcen-ID des Ereignishubs, der zum Erstellen einer Datenverbindung bzw. eines Ereignisrasters verwendet wird, ist für das Senden von Ereignissen konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="2d411-138">The resource ID of the event hub to be used to create a data connection / event grid is configured to send events.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpandedEventGrid, CreateExpandedEventHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d411-139">-EventSystemProperty</span><span class="sxs-lookup"><span data-stu-id="2d411-139">-EventSystemProperty</span></span>
<span data-ttu-id="2d411-140">Systemeigenschaften des Ereignis-/iot-Hubs.</span><span class="sxs-lookup"><span data-stu-id="2d411-140">System properties of the event/iot hub.</span></span>

```yaml
Type: System.String[]
Parameter Sets: CreateExpandedEventHub, CreateExpandedIotHub
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d411-141">-IgnoreFirstRecord</span><span class="sxs-lookup"><span data-stu-id="2d411-141">-IgnoreFirstRecord</span></span>
<span data-ttu-id="2d411-142">Wenn dies auf "true" festgelegt ist, bedeutet dies, dass die Erfassung den ersten Datensatz jeder Datei ignorieren soll.</span><span class="sxs-lookup"><span data-stu-id="2d411-142">If set to true, indicates that ingestion should ignore the first record of every file.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: UpdateExpandedEventGrid, UpdateViaIdentityExpandedEventGrid
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d411-143">-IotHubResourceId</span><span class="sxs-lookup"><span data-stu-id="2d411-143">-IotHubResourceId</span></span>
<span data-ttu-id="2d411-144">Die Ressourcen-ID des Iot-Hubs, der zum Erstellen einer Datenverbindung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="2d411-144">The resource ID of the Iot hub to be used to create a data connection.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpandedIotHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d411-145">-Kind</span><span class="sxs-lookup"><span data-stu-id="2d411-145">-Kind</span></span>
<span data-ttu-id="2d411-146">Art des Endpunkts für die Datenverbindung</span><span class="sxs-lookup"><span data-stu-id="2d411-146">Kind of the endpoint for the data connection</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.Kind
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d411-147">-Location</span><span class="sxs-lookup"><span data-stu-id="2d411-147">-Location</span></span>
<span data-ttu-id="2d411-148">Ressourcenspeicherort.</span><span class="sxs-lookup"><span data-stu-id="2d411-148">Resource location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d411-149">-MappingRuleName</span><span class="sxs-lookup"><span data-stu-id="2d411-149">-MappingRuleName</span></span>
<span data-ttu-id="2d411-150">Die Zuordnungsregel, die zum Erfassung der Daten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="2d411-150">The mapping rule to be used to ingest the data.</span></span>
<span data-ttu-id="2d411-151">Optional können die Zuordnungsinformationen jeder Nachricht hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="2d411-151">Optionally the mapping information can be added to each message.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d411-152">-Name</span><span class="sxs-lookup"><span data-stu-id="2d411-152">-Name</span></span>
<span data-ttu-id="2d411-153">Der Name der Datenverbindung.</span><span class="sxs-lookup"><span data-stu-id="2d411-153">The name of the data connection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DataConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d411-154">-NoWait</span><span class="sxs-lookup"><span data-stu-id="2d411-154">-NoWait</span></span>
<span data-ttu-id="2d411-155">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="2d411-155">Run the command asynchronously</span></span>

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

### <span data-ttu-id="2d411-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d411-156">-ResourceGroupName</span></span>
<span data-ttu-id="2d411-157">Der Name der Ressourcengruppe, die den Cluster "Kusto" enthält.</span><span class="sxs-lookup"><span data-stu-id="2d411-157">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d411-158">-SharedAccessPolicyName</span><span class="sxs-lookup"><span data-stu-id="2d411-158">-SharedAccessPolicyName</span></span>
<span data-ttu-id="2d411-159">Der Name der Freigabezugriffsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="2d411-159">The name of the share access policy.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpandedIotHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d411-160">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="2d411-160">-StorageAccountResourceId</span></span>
<span data-ttu-id="2d411-161">Die Ressourcen-ID des Speicherkontos, in dem sich die Daten befinden.</span><span class="sxs-lookup"><span data-stu-id="2d411-161">The resource ID of the storage account where the data resides.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpandedEventGrid
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d411-162">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2d411-162">-SubscriptionId</span></span>
<span data-ttu-id="2d411-163">Ruft Abonnementanmeldeinformationen ab, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="2d411-163">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="2d411-164">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="2d411-164">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d411-165">-TableName</span><span class="sxs-lookup"><span data-stu-id="2d411-165">-TableName</span></span>
<span data-ttu-id="2d411-166">Die Tabelle, in der die Daten aufgenommen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="2d411-166">The table where the data should be ingested.</span></span>
<span data-ttu-id="2d411-167">Optional können die Tabelleninformationen jeder Nachricht hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="2d411-167">Optionally the table information can be added to each message.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d411-168">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2d411-168">-Confirm</span></span>
<span data-ttu-id="2d411-169">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2d411-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2d411-170">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="2d411-170">-WhatIf</span></span>
<span data-ttu-id="2d411-171">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2d411-171">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2d411-172">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2d411-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2d411-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d411-173">CommonParameters</span></span>
<span data-ttu-id="2d411-174">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d411-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d411-175">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2d411-175">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d411-176">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2d411-176">INPUTS</span></span>

## <span data-ttu-id="2d411-177">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2d411-177">OUTPUTS</span></span>

### <span data-ttu-id="2d411-178">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDataConnection</span><span class="sxs-lookup"><span data-stu-id="2d411-178">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDataConnection</span></span>

## <span data-ttu-id="2d411-179">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="2d411-179">NOTES</span></span>

<span data-ttu-id="2d411-180">ALIASE</span><span class="sxs-lookup"><span data-stu-id="2d411-180">ALIASES</span></span>

## <span data-ttu-id="2d411-181">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="2d411-181">RELATED LINKS</span></span>

