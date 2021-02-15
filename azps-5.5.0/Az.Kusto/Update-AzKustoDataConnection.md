---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/update-azkustodataconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Update-AzKustoDataConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Update-AzKustoDataConnection.md
ms.openlocfilehash: ed697798694063c516621d25fb43e153b7a23dbc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100159569"
---
# <span data-ttu-id="02bae-101">Update-AzKustoDataConnection</span><span class="sxs-lookup"><span data-stu-id="02bae-101">Update-AzKustoDataConnection</span></span>

## <span data-ttu-id="02bae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="02bae-102">SYNOPSIS</span></span>
<span data-ttu-id="02bae-103">Aktualisiert eine Datenverbindung.</span><span class="sxs-lookup"><span data-stu-id="02bae-103">Updates a data connection.</span></span>

## <span data-ttu-id="02bae-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="02bae-104">SYNTAX</span></span>

### <span data-ttu-id="02bae-105">UpdateExpandedEventHub (Standard)</span><span class="sxs-lookup"><span data-stu-id="02bae-105">UpdateExpandedEventHub (Default)</span></span>
```
Update-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -EventHubResourceId <String> -Kind <Kind>
 -Location <String> [-SubscriptionId <String>] [-Compression <Compression>]
 [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>] [-MappingRuleName <String>]
 [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="02bae-106">UpdateExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="02bae-106">UpdateExpandedEventGrid</span></span>
```
Update-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -EventHubResourceId <String> -Kind <Kind>
 -Location <String> -StorageAccountResourceId <String> [-SubscriptionId <String>]
 [-BlobStorageEventType <BlobStorageEventType>] [-DataFormat <EventGridDataFormat>] [-IgnoreFirstRecord]
 [-MappingRuleName <String>] [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="02bae-107">UpdateExpandedIotHub</span><span class="sxs-lookup"><span data-stu-id="02bae-107">UpdateExpandedIotHub</span></span>
```
Update-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -IotHubResourceId <String> -Kind <Kind>
 -Location <String> -SharedAccessPolicyName <String> [-SubscriptionId <String>]
 [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>] [-MappingRuleName <String>]
 [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="02bae-108">UpdateViaIdentityExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="02bae-108">UpdateViaIdentityExpandedEventGrid</span></span>
```
Update-AzKustoDataConnection -InputObject <IKustoIdentity> -ConsumerGroup <String>
 -EventHubResourceId <String> -Kind <Kind> -Location <String> -StorageAccountResourceId <String>
 [-BlobStorageEventType <BlobStorageEventType>] [-DataFormat <EventGridDataFormat>] [-IgnoreFirstRecord]
 [-MappingRuleName <String>] [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="02bae-109">UpdateViaIdentityExpandedEventHub</span><span class="sxs-lookup"><span data-stu-id="02bae-109">UpdateViaIdentityExpandedEventHub</span></span>
```
Update-AzKustoDataConnection -InputObject <IKustoIdentity> -ConsumerGroup <String>
 -EventHubResourceId <String> -Kind <Kind> -Location <String> [-Compression <Compression>]
 [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>] [-MappingRuleName <String>]
 [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="02bae-110">UpdateViaIdentityExpandedIotHub</span><span class="sxs-lookup"><span data-stu-id="02bae-110">UpdateViaIdentityExpandedIotHub</span></span>
```
Update-AzKustoDataConnection -InputObject <IKustoIdentity> -ConsumerGroup <String> -IotHubResourceId <String>
 -Kind <Kind> -Location <String> -SharedAccessPolicyName <String> [-DataFormat <EventGridDataFormat>]
 [-EventSystemProperty <String[]>] [-MappingRuleName <String>] [-TableName <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="02bae-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="02bae-111">DESCRIPTION</span></span>
<span data-ttu-id="02bae-112">Aktualisiert eine Datenverbindung.</span><span class="sxs-lookup"><span data-stu-id="02bae-112">Updates a data connection.</span></span>

## <span data-ttu-id="02bae-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="02bae-113">EXAMPLES</span></span>

### <span data-ttu-id="02bae-114">Beispiel 1: Aktualisieren einer vorhandenen EventHub-Datenverbindung</span><span class="sxs-lookup"><span data-stu-id="02bae-114">Example 1: Update an existing EventHub data connection</span></span>
```powershell
PS C:\> Update-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myeventhubdc" -Location="East US" -Kind "EventHub" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -DataFormat "JSON" -ConsumerGroup '$Default' -Compression "None" -TableName "Events" -MappingRuleName "NewEventsMapping"

Kind     Location Name                                             Type
----     -------- ----                                             ----
EventHub East US  testnewkustocluster/mykustodatabase/myeventhubdc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="02bae-115">Mit dem obigen Befehl wird die vorhandene EreignisHub-Datenverbindung namens "myeventhubdc" für die Datenbank "mykustodatabase" im Cluster "testnewkustocluster" aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="02bae-115">The above command updates the existing EventHub data connection named "myeventhubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="02bae-116">Beispiel 2: Aktualisieren einer vorhandenen EventGrid-Datenverbindung</span><span class="sxs-lookup"><span data-stu-id="02bae-116">Example 2: Update an existing EventGrid data connection</span></span>
```powershell
PS C:\> Update-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myeventgriddc" -Location="East US" -Kind "EventGrid" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -StorageAccountResourceId $storageAccountResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Storage/storageAccounts/mystorage" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "NewEventsMapping"

Kind      Location Name                                              Type
----      -------- ----                                              ----
EventGrid East US  testnewkustocluster/mykustodatabase/myeventgriddc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="02bae-117">Der obige Befehl aktualisiert die vorhandene EventGrid-Datenverbindung mit dem Namen "myeventgriddc" für die Datenbank "mykustodatabase" im Cluster "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="02bae-117">The above command updates the existing EventGrid data connection named "myeventgriddc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="02bae-118">Beispiel 3: Aktualisieren einer vorhandenen IotHub-Datenverbindung</span><span class="sxs-lookup"><span data-stu-id="02bae-118">Example 3: Update an existing IotHub data connection</span></span>
```powershell
PS C:\> Update-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myiothubdc" -Location="East US" -Kind "IotHub" -IotHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Devices/IotHubs/myiothub" -SharedAccessPolicyName "myiothubpolicy" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "NewEventsMapping"

Kind      Location Name                                        Type
----      -------- ----                                        ----
IotHub East US  testnewkustocluster/mykustodatabase/myiothubdc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="02bae-119">Der obige Befehl aktualisiert die vorhandene IotHub-Datenverbindung mit dem Namen "myiothubdc" für die Datenbank "mykustodatabase" im Cluster "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="02bae-119">The above command updates the existing IotHub data connection named "myiothubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="02bae-120">Beispiel 4: Aktualisieren einer vorhandenen EventHub-Datenverbindung über Identität</span><span class="sxs-lookup"><span data-stu-id="02bae-120">Example 4: Update an existing EventHub data connection via identity</span></span>
```powershell
PS C:\> $dataConnection = Get-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myeventhubdc" 
PS C:\> Update-AzKustoDataConnection -InputObject $dataConnection -Location="East US" -Kind "EventHub" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -DataFormat "JSON" -ConsumerGroup '$Default' -Compression "None" -TableName "Events" -MappingRuleName "NewEventsMapping"

Kind     Location Name                                             Type
----     -------- ----                                             ----
EventHub East US  testnewkustocluster/mykustodatabase/myeventhubdc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="02bae-121">Mit dem obigen Befehl wird die vorhandene EreignisHub-Datenverbindung namens "myeventhubdc" für die Datenbank "mykustodatabase" im Cluster "testnewkustocluster" aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="02bae-121">The above command updates the existing EventHub data connection named "myeventhubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="02bae-122">Beispiel 5: Aktualisieren einer vorhandenen EventGrid-Datenverbindung über Identität</span><span class="sxs-lookup"><span data-stu-id="02bae-122">Example 5: Update an existing EventGrid data connection via identity</span></span>
```powershell
PS C:\> $dataConnection = Get-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myeventgriddc" 
PS C:\> Update-AzKustoDataConnection -InputObject $dataConnection -Location="East US" -Kind "EventGrid" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -StorageAccountResourceId $storageAccountResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Storage/storageAccounts/mystorage" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "NewEventsMapping"

Kind      Location Name                                              Type
----      -------- ----                                              ----
EventGrid East US  testnewkustocluster/mykustodatabase/myeventgriddc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="02bae-123">Der obige Befehl aktualisiert die vorhandene EventGrid-Datenverbindung mit dem Namen "myeventgriddc" für die Datenbank "mykustodatabase" im Cluster "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="02bae-123">The above command updates the existing EventGrid data connection named "myeventgriddc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="02bae-124">Beispiel 6: Aktualisieren einer vorhandenen IotHub-Datenverbindung über Identität</span><span class="sxs-lookup"><span data-stu-id="02bae-124">Example 6: Update an existing IotHub data connection via identity</span></span>
```powershell
PS C:\> $dataConnection = Get-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myiothubdc" 
PS C:\> Update-AzKustoDataConnection -InputObject $dataConnection -Location="East US" -Kind "IotHub" -IotHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Devices/IotHubs/myiothub" -SharedAccessPolicyName "myiothubpolicy" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "NewEventsMapping"

Kind      Location Name                                        Type
----      -------- ----                                        ----
IotHub East US  testnewkustocluster/mykustodatabase/myiothubdc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="02bae-125">Der obige Befehl aktualisiert die vorhandene IotHub-Datenverbindung mit dem Namen "myiothubdc" für die Datenbank "mykustodatabase" im Cluster "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="02bae-125">The above command updates the existing IotHub data connection named "myiothubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

## <span data-ttu-id="02bae-126">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="02bae-126">PARAMETERS</span></span>

### <span data-ttu-id="02bae-127">-AsJob</span><span class="sxs-lookup"><span data-stu-id="02bae-127">-AsJob</span></span>
<span data-ttu-id="02bae-128">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="02bae-128">Run the command as a job</span></span>

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

### <span data-ttu-id="02bae-129">-BlobStorageEventType</span><span class="sxs-lookup"><span data-stu-id="02bae-129">-BlobStorageEventType</span></span>
<span data-ttu-id="02bae-130">Der Name des zu verarbeitende BLOB-Speicherereignistyps.</span><span class="sxs-lookup"><span data-stu-id="02bae-130">The name of blob storage event type to process.</span></span>

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

### <span data-ttu-id="02bae-131">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="02bae-131">-ClusterName</span></span>
<span data-ttu-id="02bae-132">Der Name des Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="02bae-132">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpandedEventGrid, UpdateExpandedEventHub, UpdateExpandedIotHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02bae-133">-Compression</span><span class="sxs-lookup"><span data-stu-id="02bae-133">-Compression</span></span>
<span data-ttu-id="02bae-134">Der Komprimierungstyp für Ereignishubnachrichten.</span><span class="sxs-lookup"><span data-stu-id="02bae-134">The event hub messages compression type.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.Compression
Parameter Sets: UpdateExpandedEventHub, UpdateViaIdentityExpandedEventHub
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02bae-135">-ConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="02bae-135">-ConsumerGroup</span></span>
<span data-ttu-id="02bae-136">Die Consumergruppe "Ereignis/iot-Hub".</span><span class="sxs-lookup"><span data-stu-id="02bae-136">The event/iot hub consumer group.</span></span>

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

### <span data-ttu-id="02bae-137">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="02bae-137">-DatabaseName</span></span>
<span data-ttu-id="02bae-138">Der Name der Datenbank im Cluster "Kusto".</span><span class="sxs-lookup"><span data-stu-id="02bae-138">The name of the database in the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpandedEventGrid, UpdateExpandedEventHub, UpdateExpandedIotHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02bae-139">-DataFormat</span><span class="sxs-lookup"><span data-stu-id="02bae-139">-DataFormat</span></span>
<span data-ttu-id="02bae-140">Das Datenformat der Nachricht.</span><span class="sxs-lookup"><span data-stu-id="02bae-140">The data format of the message.</span></span>
<span data-ttu-id="02bae-141">Optional kann jeder Nachricht das Datenformat hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="02bae-141">Optionally the data format can be added to each message.</span></span>

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

### <span data-ttu-id="02bae-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02bae-142">-DefaultProfile</span></span>
<span data-ttu-id="02bae-143">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="02bae-143">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="02bae-144">-EventHubResourceId</span><span class="sxs-lookup"><span data-stu-id="02bae-144">-EventHubResourceId</span></span>
<span data-ttu-id="02bae-145">Die Ressourcen-ID des Ereignishubs, der zum Erstellen einer Datenverbindung bzw. eines Ereignisrasters verwendet wird, ist für das Senden von Ereignissen konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="02bae-145">The resource ID of the event hub to be used to create a data connection / event grid is configured to send events.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpandedEventGrid, UpdateExpandedEventHub, UpdateViaIdentityExpandedEventGrid, UpdateViaIdentityExpandedEventHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02bae-146">-EventSystemProperty</span><span class="sxs-lookup"><span data-stu-id="02bae-146">-EventSystemProperty</span></span>
<span data-ttu-id="02bae-147">Systemeigenschaften des Ereignis-/iot-Hubs.</span><span class="sxs-lookup"><span data-stu-id="02bae-147">System properties of the event/iot hub.</span></span>

```yaml
Type: System.String[]
Parameter Sets: UpdateExpandedEventHub, UpdateExpandedIotHub, UpdateViaIdentityExpandedEventHub, UpdateViaIdentityExpandedIotHub
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02bae-148">-IgnoreFirstRecord</span><span class="sxs-lookup"><span data-stu-id="02bae-148">-IgnoreFirstRecord</span></span>
<span data-ttu-id="02bae-149">Wenn dies auf "true" festgelegt ist, bedeutet dies, dass die Erfassung den ersten Datensatz jeder Datei ignorieren soll.</span><span class="sxs-lookup"><span data-stu-id="02bae-149">If set to true, indicates that ingestion should ignore the first record of every file.</span></span>

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

### <span data-ttu-id="02bae-150">-InputObject</span><span class="sxs-lookup"><span data-stu-id="02bae-150">-InputObject</span></span>
<span data-ttu-id="02bae-151">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="02bae-151">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: UpdateViaIdentityExpandedEventGrid, UpdateViaIdentityExpandedEventHub, UpdateViaIdentityExpandedIotHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="02bae-152">-IotHubResourceId</span><span class="sxs-lookup"><span data-stu-id="02bae-152">-IotHubResourceId</span></span>
<span data-ttu-id="02bae-153">Die Ressourcen-ID des Iot-Hubs, der zum Erstellen einer Datenverbindung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="02bae-153">The resource ID of the Iot hub to be used to create a data connection.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpandedIotHub, UpdateViaIdentityExpandedIotHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02bae-154">-Kind</span><span class="sxs-lookup"><span data-stu-id="02bae-154">-Kind</span></span>
<span data-ttu-id="02bae-155">Art des Endpunkts für die Datenverbindung</span><span class="sxs-lookup"><span data-stu-id="02bae-155">Kind of the endpoint for the data connection</span></span>

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

### <span data-ttu-id="02bae-156">-Location</span><span class="sxs-lookup"><span data-stu-id="02bae-156">-Location</span></span>
<span data-ttu-id="02bae-157">Ressourcenspeicherort.</span><span class="sxs-lookup"><span data-stu-id="02bae-157">Resource location.</span></span>

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

### <span data-ttu-id="02bae-158">-MappingRuleName</span><span class="sxs-lookup"><span data-stu-id="02bae-158">-MappingRuleName</span></span>
<span data-ttu-id="02bae-159">Die Zuordnungsregel, die zum Erfassung der Daten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="02bae-159">The mapping rule to be used to ingest the data.</span></span>
<span data-ttu-id="02bae-160">Optional können die Zuordnungsinformationen jeder Nachricht hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="02bae-160">Optionally the mapping information can be added to each message.</span></span>

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

### <span data-ttu-id="02bae-161">-Name</span><span class="sxs-lookup"><span data-stu-id="02bae-161">-Name</span></span>
<span data-ttu-id="02bae-162">Der Name der Datenverbindung.</span><span class="sxs-lookup"><span data-stu-id="02bae-162">The name of the data connection.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpandedEventGrid, UpdateExpandedEventHub, UpdateExpandedIotHub
Aliases: DataConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02bae-163">-NoWait</span><span class="sxs-lookup"><span data-stu-id="02bae-163">-NoWait</span></span>
<span data-ttu-id="02bae-164">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="02bae-164">Run the command asynchronously</span></span>

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

### <span data-ttu-id="02bae-165">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02bae-165">-ResourceGroupName</span></span>
<span data-ttu-id="02bae-166">Der Name der Ressourcengruppe, die den Cluster "Kusto" enthält.</span><span class="sxs-lookup"><span data-stu-id="02bae-166">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpandedEventGrid, UpdateExpandedEventHub, UpdateExpandedIotHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02bae-167">-SharedAccessPolicyName</span><span class="sxs-lookup"><span data-stu-id="02bae-167">-SharedAccessPolicyName</span></span>
<span data-ttu-id="02bae-168">Der Name der Freigabezugriffsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="02bae-168">The name of the share access policy.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpandedIotHub, UpdateViaIdentityExpandedIotHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02bae-169">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="02bae-169">-StorageAccountResourceId</span></span>
<span data-ttu-id="02bae-170">Die Ressourcen-ID des Speicherkontos, in dem sich die Daten befinden.</span><span class="sxs-lookup"><span data-stu-id="02bae-170">The resource ID of the storage account where the data resides.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpandedEventGrid, UpdateViaIdentityExpandedEventGrid
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02bae-171">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="02bae-171">-SubscriptionId</span></span>
<span data-ttu-id="02bae-172">Ruft Abonnementanmeldeinformationen ab, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="02bae-172">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="02bae-173">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="02bae-173">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpandedEventGrid, UpdateExpandedEventHub, UpdateExpandedIotHub
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02bae-174">-TableName</span><span class="sxs-lookup"><span data-stu-id="02bae-174">-TableName</span></span>
<span data-ttu-id="02bae-175">Die Tabelle, in der die Daten aufgenommen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="02bae-175">The table where the data should be ingested.</span></span>
<span data-ttu-id="02bae-176">Optional können die Tabelleninformationen jeder Nachricht hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="02bae-176">Optionally the table information can be added to each message.</span></span>

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

### <span data-ttu-id="02bae-177">-Confirm</span><span class="sxs-lookup"><span data-stu-id="02bae-177">-Confirm</span></span>
<span data-ttu-id="02bae-178">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="02bae-178">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02bae-179">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="02bae-179">-WhatIf</span></span>
<span data-ttu-id="02bae-180">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="02bae-180">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="02bae-181">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="02bae-181">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02bae-182">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02bae-182">CommonParameters</span></span>
<span data-ttu-id="02bae-183">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02bae-183">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02bae-184">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="02bae-184">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02bae-185">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="02bae-185">INPUTS</span></span>

### <span data-ttu-id="02bae-186">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="02bae-186">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="02bae-187">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="02bae-187">OUTPUTS</span></span>

### <span data-ttu-id="02bae-188">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDataConnection</span><span class="sxs-lookup"><span data-stu-id="02bae-188">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDataConnection</span></span>

## <span data-ttu-id="02bae-189">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="02bae-189">NOTES</span></span>

<span data-ttu-id="02bae-190">ALIASE</span><span class="sxs-lookup"><span data-stu-id="02bae-190">ALIASES</span></span>

<span data-ttu-id="02bae-191">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="02bae-191">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="02bae-192">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="02bae-192">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="02bae-193">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="02bae-193">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="02bae-194">INPUTOBJECT <IKustoIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="02bae-194">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="02bae-195">`[AttachedDatabaseConfigurationName <String>]`: Der Name der angefügten Datenbankkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="02bae-195">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="02bae-196">`[ClusterName <String>]`: Der Name des Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="02bae-196">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="02bae-197">`[DataConnectionName <String>]`: Der Name der Datenverbindung.</span><span class="sxs-lookup"><span data-stu-id="02bae-197">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="02bae-198">`[DatabaseName <String>]`: Der Name der Datenbank im Cluster "Kusto".</span><span class="sxs-lookup"><span data-stu-id="02bae-198">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="02bae-199">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="02bae-199">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="02bae-200">`[Location <String>]`: Azure-Standort.</span><span class="sxs-lookup"><span data-stu-id="02bae-200">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="02bae-201">`[PrincipalAssignmentName <String>]`: Der Name der Kusto PrincipalAssignment.</span><span class="sxs-lookup"><span data-stu-id="02bae-201">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="02bae-202">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die den Cluster "Kusto" enthält.</span><span class="sxs-lookup"><span data-stu-id="02bae-202">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="02bae-203">`[SubscriptionId <String>]`: Ruft Abonnementanmeldeinformationen ab, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="02bae-203">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="02bae-204">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="02bae-204">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="02bae-205">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="02bae-205">RELATED LINKS</span></span>

