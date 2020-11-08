---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/update-azkustodataconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Update-AzKustoDataConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Update-AzKustoDataConnection.md
ms.openlocfilehash: 70862dee30fd03430d93de88e1e63f0f5acf5e6c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174699"
---
# <span data-ttu-id="d90df-101">Update-AzKustoDataConnection</span><span class="sxs-lookup"><span data-stu-id="d90df-101">Update-AzKustoDataConnection</span></span>

## <span data-ttu-id="d90df-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d90df-102">SYNOPSIS</span></span>
<span data-ttu-id="d90df-103">Aktualisiert eine Datenverbindung.</span><span class="sxs-lookup"><span data-stu-id="d90df-103">Updates a data connection.</span></span>

## <span data-ttu-id="d90df-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d90df-104">SYNTAX</span></span>

### <span data-ttu-id="d90df-105">UpdateExpandedEventHub (Standard)</span><span class="sxs-lookup"><span data-stu-id="d90df-105">UpdateExpandedEventHub (Default)</span></span>
```
Update-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -EventHubResourceId <String> -Kind <Kind>
 -Location <String> [-SubscriptionId <String>] [-Compression <Compression>]
 [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>] [-MappingRuleName <String>]
 [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="d90df-106">UpdateExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="d90df-106">UpdateExpandedEventGrid</span></span>
```
Update-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -EventHubResourceId <String> -Kind <Kind>
 -Location <String> -StorageAccountResourceId <String> [-SubscriptionId <String>]
 [-BlobStorageEventType <BlobStorageEventType>] [-DataFormat <EventGridDataFormat>] [-IgnoreFirstRecord]
 [-MappingRuleName <String>] [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d90df-107">UpdateExpandedIotHub</span><span class="sxs-lookup"><span data-stu-id="d90df-107">UpdateExpandedIotHub</span></span>
```
Update-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -IotHubResourceId <String> -Kind <Kind>
 -Location <String> -SharedAccessPolicyName <String> [-SubscriptionId <String>]
 [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>] [-MappingRuleName <String>]
 [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="d90df-108">UpdateViaIdentityExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="d90df-108">UpdateViaIdentityExpandedEventGrid</span></span>
```
Update-AzKustoDataConnection -InputObject <IKustoIdentity> -ConsumerGroup <String>
 -EventHubResourceId <String> -Kind <Kind> -Location <String> -StorageAccountResourceId <String>
 [-BlobStorageEventType <BlobStorageEventType>] [-DataFormat <EventGridDataFormat>] [-IgnoreFirstRecord]
 [-MappingRuleName <String>] [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d90df-109">UpdateViaIdentityExpandedEventHub</span><span class="sxs-lookup"><span data-stu-id="d90df-109">UpdateViaIdentityExpandedEventHub</span></span>
```
Update-AzKustoDataConnection -InputObject <IKustoIdentity> -ConsumerGroup <String>
 -EventHubResourceId <String> -Kind <Kind> -Location <String> [-Compression <Compression>]
 [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>] [-MappingRuleName <String>]
 [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="d90df-110">UpdateViaIdentityExpandedIotHub</span><span class="sxs-lookup"><span data-stu-id="d90df-110">UpdateViaIdentityExpandedIotHub</span></span>
```
Update-AzKustoDataConnection -InputObject <IKustoIdentity> -ConsumerGroup <String> -IotHubResourceId <String>
 -Kind <Kind> -Location <String> -SharedAccessPolicyName <String> [-DataFormat <EventGridDataFormat>]
 [-EventSystemProperty <String[]>] [-MappingRuleName <String>] [-TableName <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d90df-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d90df-111">DESCRIPTION</span></span>
<span data-ttu-id="d90df-112">Aktualisiert eine Datenverbindung.</span><span class="sxs-lookup"><span data-stu-id="d90df-112">Updates a data connection.</span></span>

## <span data-ttu-id="d90df-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d90df-113">EXAMPLES</span></span>

### <span data-ttu-id="d90df-114">Beispiel 1: Aktualisieren einer vorhandenen EventHub-Datenverbindung</span><span class="sxs-lookup"><span data-stu-id="d90df-114">Example 1: Update an existing EventHub data connection</span></span>
```powershell
PS C:\> Update-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myeventhubdc" -Location="East US" -Kind "EventHub" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -DataFormat "JSON" -ConsumerGroup '$Default' -Compression "None" -TableName "Events" -MappingRuleName "NewEventsMapping"

Kind     Location Name                                             Type
----     -------- ----                                             ----
EventHub East US  testnewkustocluster/mykustodatabase/myeventhubdc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="d90df-115">Der obige Befehl aktualisiert die vorhandene EventHub-Datenverbindung mit dem Namen "myeventhubdc" für die Datenbank "mykustodatabase" im Cluster "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="d90df-115">The above command updates the existing EventHub data connection named "myeventhubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="d90df-116">Beispiel 2: Aktualisieren einer vorhandenen EventGrid-Datenverbindung</span><span class="sxs-lookup"><span data-stu-id="d90df-116">Example 2: Update an existing EventGrid data connection</span></span>
```powershell
PS C:\> Update-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myeventgriddc" -Location="East US" -Kind "EventGrid" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -StorageAccountResourceId $storageAccountResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Storage/storageAccounts/mystorage" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "NewEventsMapping"

Kind      Location Name                                              Type
----      -------- ----                                              ----
EventGrid East US  testnewkustocluster/mykustodatabase/myeventgriddc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="d90df-117">Der obige Befehl aktualisiert die vorhandene EventGrid-Datenverbindung mit dem Namen "myeventgriddc" für die Datenbank "mykustodatabase" im Cluster "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="d90df-117">The above command updates the existing EventGrid data connection named "myeventgriddc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="d90df-118">Beispiel 3: Aktualisieren einer vorhandenen IotHub-Datenverbindung</span><span class="sxs-lookup"><span data-stu-id="d90df-118">Example 3: Update an existing IotHub data connection</span></span>
```powershell
PS C:\> Update-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myiothubdc" -Location="East US" -Kind "IotHub" -IotHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Devices/IotHubs/myiothub" -SharedAccessPolicyName "myiothubpolicy" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "NewEventsMapping"

Kind      Location Name                                        Type
----      -------- ----                                        ----
IotHub East US  testnewkustocluster/mykustodatabase/myiothubdc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="d90df-119">Der obige Befehl aktualisiert die vorhandene IotHub-Datenverbindung mit dem Namen "myiothubdc" für die Datenbank "mykustodatabase" im Cluster "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="d90df-119">The above command updates the existing IotHub data connection named "myiothubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="d90df-120">Beispiel 4: Aktualisieren einer vorhandenen EventHub-Datenverbindung über die Identität</span><span class="sxs-lookup"><span data-stu-id="d90df-120">Example 4: Update an existing EventHub data connection via identity</span></span>
```powershell
PS C:\> $dataConnection = Get-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myeventhubdc" 
PS C:\> Update-AzKustoDataConnection -InputObject $dataConnection -Location="East US" -Kind "EventHub" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -DataFormat "JSON" -ConsumerGroup '$Default' -Compression "None" -TableName "Events" -MappingRuleName "NewEventsMapping"

Kind     Location Name                                             Type
----     -------- ----                                             ----
EventHub East US  testnewkustocluster/mykustodatabase/myeventhubdc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="d90df-121">Der obige Befehl aktualisiert die vorhandene EventHub-Datenverbindung mit dem Namen "myeventhubdc" für die Datenbank "mykustodatabase" im Cluster "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="d90df-121">The above command updates the existing EventHub data connection named "myeventhubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="d90df-122">Beispiel 5: Aktualisieren einer vorhandenen EventGrid-Datenverbindung über die Identität</span><span class="sxs-lookup"><span data-stu-id="d90df-122">Example 5: Update an existing EventGrid data connection via identity</span></span>
```powershell
PS C:\> $dataConnection = Get-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myeventgriddc" 
PS C:\> Update-AzKustoDataConnection -InputObject $dataConnection -Location="East US" -Kind "EventGrid" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -StorageAccountResourceId $storageAccountResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Storage/storageAccounts/mystorage" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "NewEventsMapping"

Kind      Location Name                                              Type
----      -------- ----                                              ----
EventGrid East US  testnewkustocluster/mykustodatabase/myeventgriddc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="d90df-123">Der obige Befehl aktualisiert die vorhandene EventGrid-Datenverbindung mit dem Namen "myeventgriddc" für die Datenbank "mykustodatabase" im Cluster "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="d90df-123">The above command updates the existing EventGrid data connection named "myeventgriddc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="d90df-124">Beispiel 6: Aktualisieren einer vorhandenen IotHub-Datenverbindung über die Identität</span><span class="sxs-lookup"><span data-stu-id="d90df-124">Example 6: Update an existing IotHub data connection via identity</span></span>
```powershell
PS C:\> $dataConnection = Get-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myiothubdc" 
PS C:\> Update-AzKustoDataConnection -InputObject $dataConnection -Location="East US" -Kind "IotHub" -IotHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Devices/IotHubs/myiothub" -SharedAccessPolicyName "myiothubpolicy" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "NewEventsMapping"

Kind      Location Name                                        Type
----      -------- ----                                        ----
IotHub East US  testnewkustocluster/mykustodatabase/myiothubdc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="d90df-125">Der obige Befehl aktualisiert die vorhandene IotHub-Datenverbindung mit dem Namen "myiothubdc" für die Datenbank "mykustodatabase" im Cluster "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="d90df-125">The above command updates the existing IotHub data connection named "myiothubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

## <span data-ttu-id="d90df-126">Parameter</span><span class="sxs-lookup"><span data-stu-id="d90df-126">PARAMETERS</span></span>

### <span data-ttu-id="d90df-127">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d90df-127">-AsJob</span></span>
<span data-ttu-id="d90df-128">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="d90df-128">Run the command as a job</span></span>

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

### <span data-ttu-id="d90df-129">-BlobStorageEventType</span><span class="sxs-lookup"><span data-stu-id="d90df-129">-BlobStorageEventType</span></span>
<span data-ttu-id="d90df-130">Der Name des zu verarbeitenden BLOB-Speicherereignis Typs.</span><span class="sxs-lookup"><span data-stu-id="d90df-130">The name of blob storage event type to process.</span></span>

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

### <span data-ttu-id="d90df-131">-Clustername</span><span class="sxs-lookup"><span data-stu-id="d90df-131">-ClusterName</span></span>
<span data-ttu-id="d90df-132">Der Name des Kusto-Clusters.</span><span class="sxs-lookup"><span data-stu-id="d90df-132">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="d90df-133">-Komprimierung</span><span class="sxs-lookup"><span data-stu-id="d90df-133">-Compression</span></span>
<span data-ttu-id="d90df-134">Der Komprimierungstyp des Ereignis-Hub-Nachrichtentyps.</span><span class="sxs-lookup"><span data-stu-id="d90df-134">The event hub messages compression type.</span></span>

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

### <span data-ttu-id="d90df-135">-Consumergroup</span><span class="sxs-lookup"><span data-stu-id="d90df-135">-ConsumerGroup</span></span>
<span data-ttu-id="d90df-136">Die Verbrauchergruppe "Event/viel Hub"</span><span class="sxs-lookup"><span data-stu-id="d90df-136">The event/iot hub consumer group.</span></span>

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

### <span data-ttu-id="d90df-137">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d90df-137">-DatabaseName</span></span>
<span data-ttu-id="d90df-138">Der Name der Datenbank im Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="d90df-138">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="d90df-139">-DataFormat</span><span class="sxs-lookup"><span data-stu-id="d90df-139">-DataFormat</span></span>
<span data-ttu-id="d90df-140">Das Datenformat der Nachricht.</span><span class="sxs-lookup"><span data-stu-id="d90df-140">The data format of the message.</span></span>
<span data-ttu-id="d90df-141">Optional kann das Datenformat jeder Nachricht hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="d90df-141">Optionally the data format can be added to each message.</span></span>

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

### <span data-ttu-id="d90df-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d90df-142">-DefaultProfile</span></span>
<span data-ttu-id="d90df-143">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d90df-143">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d90df-144">-EventHubResourceId</span><span class="sxs-lookup"><span data-stu-id="d90df-144">-EventHubResourceId</span></span>
<span data-ttu-id="d90df-145">Die Ressourcen-ID des Ereignis Hubs, der zum Erstellen eines Daten Verbindungs-/Ereignis Rasters verwendet werden soll, ist für das Senden von Ereignissen konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="d90df-145">The resource ID of the event hub to be used to create a data connection / event grid is configured to send events.</span></span>

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

### <span data-ttu-id="d90df-146">-EventSystemProperty</span><span class="sxs-lookup"><span data-stu-id="d90df-146">-EventSystemProperty</span></span>
<span data-ttu-id="d90df-147">System Eigenschaften des Event/viele-Hubs</span><span class="sxs-lookup"><span data-stu-id="d90df-147">System properties of the event/iot hub.</span></span>

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

### <span data-ttu-id="d90df-148">-IgnoreFirstRecord</span><span class="sxs-lookup"><span data-stu-id="d90df-148">-IgnoreFirstRecord</span></span>
<span data-ttu-id="d90df-149">Ist auf "true" festgelegt, gibt an, dass die Einnahme den ersten Datensatz jeder Datei ignorieren soll.</span><span class="sxs-lookup"><span data-stu-id="d90df-149">If set to true, indicates that ingestion should ignore the first record of every file.</span></span>

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

### <span data-ttu-id="d90df-150">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="d90df-150">-InputObject</span></span>
<span data-ttu-id="d90df-151">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="d90df-151">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="d90df-152">-IotHubResourceId</span><span class="sxs-lookup"><span data-stu-id="d90df-152">-IotHubResourceId</span></span>
<span data-ttu-id="d90df-153">Die Ressourcen-ID des viel-Hubs, der zum Erstellen einer Datenverbindung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d90df-153">The resource ID of the Iot hub to be used to create a data connection.</span></span>

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

### <span data-ttu-id="d90df-154">-Art</span><span class="sxs-lookup"><span data-stu-id="d90df-154">-Kind</span></span>
<span data-ttu-id="d90df-155">Art des Endpunkts für die Datenverbindung</span><span class="sxs-lookup"><span data-stu-id="d90df-155">Kind of the endpoint for the data connection</span></span>

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

### <span data-ttu-id="d90df-156">-Standort</span><span class="sxs-lookup"><span data-stu-id="d90df-156">-Location</span></span>
<span data-ttu-id="d90df-157">Ressourcen Standort.</span><span class="sxs-lookup"><span data-stu-id="d90df-157">Resource location.</span></span>

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

### <span data-ttu-id="d90df-158">-MappingRuleName</span><span class="sxs-lookup"><span data-stu-id="d90df-158">-MappingRuleName</span></span>
<span data-ttu-id="d90df-159">Die Zuordnungsregel, die zum Aufnehmen der Daten verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d90df-159">The mapping rule to be used to ingest the data.</span></span>
<span data-ttu-id="d90df-160">Optional können die Zuordnungsinformationen jeder Nachricht hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="d90df-160">Optionally the mapping information can be added to each message.</span></span>

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

### <span data-ttu-id="d90df-161">-Name</span><span class="sxs-lookup"><span data-stu-id="d90df-161">-Name</span></span>
<span data-ttu-id="d90df-162">Der Name der Datenverbindung.</span><span class="sxs-lookup"><span data-stu-id="d90df-162">The name of the data connection.</span></span>

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

### <span data-ttu-id="d90df-163">-Nowait</span><span class="sxs-lookup"><span data-stu-id="d90df-163">-NoWait</span></span>
<span data-ttu-id="d90df-164">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="d90df-164">Run the command asynchronously</span></span>

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

### <span data-ttu-id="d90df-165">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d90df-165">-ResourceGroupName</span></span>
<span data-ttu-id="d90df-166">Der Name der Ressourcengruppe, die den Kusto-Cluster enthält.</span><span class="sxs-lookup"><span data-stu-id="d90df-166">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="d90df-167">-SharedAccessPolicyName</span><span class="sxs-lookup"><span data-stu-id="d90df-167">-SharedAccessPolicyName</span></span>
<span data-ttu-id="d90df-168">Der Name der Freigabe Zugriffsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="d90df-168">The name of the share access policy.</span></span>

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

### <span data-ttu-id="d90df-169">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="d90df-169">-StorageAccountResourceId</span></span>
<span data-ttu-id="d90df-170">Die Ressourcen-ID des speicherkontos, in dem sich die Daten befinden.</span><span class="sxs-lookup"><span data-stu-id="d90df-170">The resource ID of the storage account where the data resides.</span></span>

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

### <span data-ttu-id="d90df-171">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="d90df-171">-SubscriptionId</span></span>
<span data-ttu-id="d90df-172">Ruft Abonnement Anmeldeinformationen ab, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="d90df-172">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="d90df-173">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="d90df-173">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="d90df-174">-Tabellenname</span><span class="sxs-lookup"><span data-stu-id="d90df-174">-TableName</span></span>
<span data-ttu-id="d90df-175">Die Tabelle, in der die Daten aufgenommen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d90df-175">The table where the data should be ingested.</span></span>
<span data-ttu-id="d90df-176">Optional können die Tabelleninformationen zu den einzelnen Nachrichten hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="d90df-176">Optionally the table information can be added to each message.</span></span>

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

### <span data-ttu-id="d90df-177">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d90df-177">-Confirm</span></span>
<span data-ttu-id="d90df-178">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d90df-178">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d90df-179">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d90df-179">-WhatIf</span></span>
<span data-ttu-id="d90df-180">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d90df-180">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d90df-181">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d90df-181">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d90df-182">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d90df-182">CommonParameters</span></span>
<span data-ttu-id="d90df-183">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d90df-183">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d90df-184">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d90df-184">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d90df-185">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d90df-185">INPUTS</span></span>

### <span data-ttu-id="d90df-186">Microsoft. Azure. PowerShell. Cmdlets. Kusto. Models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="d90df-186">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="d90df-187">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d90df-187">OUTPUTS</span></span>

### <span data-ttu-id="d90df-188">Microsoft. Azure. PowerShell. Cmdlets. Kusto. Models. Api20200614. IDataConnection</span><span class="sxs-lookup"><span data-stu-id="d90df-188">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IDataConnection</span></span>

## <span data-ttu-id="d90df-189">Notizen</span><span class="sxs-lookup"><span data-stu-id="d90df-189">NOTES</span></span>

<span data-ttu-id="d90df-190">Aliase</span><span class="sxs-lookup"><span data-stu-id="d90df-190">ALIASES</span></span>

<span data-ttu-id="d90df-191">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d90df-191">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d90df-192">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="d90df-192">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d90df-193">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="d90df-193">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d90df-194">Inputobject <IKustoIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="d90df-194">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d90df-195">`[AttachedDatabaseConfigurationName <String>]`: Der Name der angefügten Datenbankkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="d90df-195">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="d90df-196">`[ClusterName <String>]`: Der Name des Kusto-Clusters.</span><span class="sxs-lookup"><span data-stu-id="d90df-196">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="d90df-197">`[DataConnectionName <String>]`: Der Name der Datenverbindung.</span><span class="sxs-lookup"><span data-stu-id="d90df-197">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="d90df-198">`[DatabaseName <String>]`: Der Name der Datenbank im Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="d90df-198">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="d90df-199">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="d90df-199">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d90df-200">`[Location <String>]`: Azure-Position.</span><span class="sxs-lookup"><span data-stu-id="d90df-200">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="d90df-201">`[PrincipalAssignmentName <String>]`: Der Name des Kusto-principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="d90df-201">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="d90df-202">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die den Kusto-Cluster enthält.</span><span class="sxs-lookup"><span data-stu-id="d90df-202">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="d90df-203">`[SubscriptionId <String>]`: Ruft Abonnement Anmeldeinformationen ab, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="d90df-203">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="d90df-204">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="d90df-204">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="d90df-205">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d90df-205">RELATED LINKS</span></span>

