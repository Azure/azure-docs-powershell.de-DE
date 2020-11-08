---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/invoke-azkustodataconnectionvalidation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Invoke-AzKustoDataConnectionValidation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Invoke-AzKustoDataConnectionValidation.md
ms.openlocfilehash: 9eb3ff31873b23fc97f53fffecdbbb38367ac2b5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94179211"
---
# <span data-ttu-id="51b93-101">Invoke-AzKustoDataConnectionValidation</span><span class="sxs-lookup"><span data-stu-id="51b93-101">Invoke-AzKustoDataConnectionValidation</span></span>

## <span data-ttu-id="51b93-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="51b93-102">SYNOPSIS</span></span>
<span data-ttu-id="51b93-103">Überprüft, ob die Datenverbindungsparameter gültig sind.</span><span class="sxs-lookup"><span data-stu-id="51b93-103">Checks that the data connection parameters are valid.</span></span>

## <span data-ttu-id="51b93-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="51b93-104">SYNTAX</span></span>

### <span data-ttu-id="51b93-105">DataExpandedEventHub (Standard)</span><span class="sxs-lookup"><span data-stu-id="51b93-105">DataExpandedEventHub (Default)</span></span>
```
Invoke-AzKustoDataConnectionValidation -ClusterName <String> -DatabaseName <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -DataConnectionName <String> -EventHubResourceId <String>
 -Kind <Kind> -Location <String> [-SubscriptionId <String>] [-Compression <Compression>]
 [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>] [-MappingRuleName <String>]
 [-TableName <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="51b93-106">DataExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="51b93-106">DataExpandedEventGrid</span></span>
```
Invoke-AzKustoDataConnectionValidation -ClusterName <String> -DatabaseName <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -DataConnectionName <String> -EventHubResourceId <String>
 -Kind <Kind> -Location <String> -StorageAccountResourceId <String> [-SubscriptionId <String>]
 [-DataFormat <EventGridDataFormat>] [-MappingRuleName <String>] [-TableName <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="51b93-107">DataExpandedIotHub</span><span class="sxs-lookup"><span data-stu-id="51b93-107">DataExpandedIotHub</span></span>
```
Invoke-AzKustoDataConnectionValidation -ClusterName <String> -DatabaseName <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -DataConnectionName <String> -IotHubResourceId <String>
 -Kind <Kind> -Location <String> -SharedAccessPolicyName <String> [-SubscriptionId <String>]
 [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>] [-MappingRuleName <String>]
 [-TableName <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="51b93-108">DataViaIdentityExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="51b93-108">DataViaIdentityExpandedEventGrid</span></span>
```
Invoke-AzKustoDataConnectionValidation -InputObject <IKustoIdentity> -ConsumerGroup <String>
 -DataConnectionName <String> -EventHubResourceId <String> -Kind <Kind> -Location <String>
 -StorageAccountResourceId <String> [-DataFormat <EventGridDataFormat>] [-MappingRuleName <String>]
 [-TableName <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="51b93-109">DataViaIdentityExpandedEventHub</span><span class="sxs-lookup"><span data-stu-id="51b93-109">DataViaIdentityExpandedEventHub</span></span>
```
Invoke-AzKustoDataConnectionValidation -InputObject <IKustoIdentity> -ConsumerGroup <String>
 -DataConnectionName <String> -EventHubResourceId <String> -Kind <Kind> -Location <String>
 [-Compression <Compression>] [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>]
 [-MappingRuleName <String>] [-TableName <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="51b93-110">DataViaIdentityExpandedIotHub</span><span class="sxs-lookup"><span data-stu-id="51b93-110">DataViaIdentityExpandedIotHub</span></span>
```
Invoke-AzKustoDataConnectionValidation -InputObject <IKustoIdentity> -ConsumerGroup <String>
 -DataConnectionName <String> -IotHubResourceId <String> -Kind <Kind> -Location <String>
 -SharedAccessPolicyName <String> [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>]
 [-MappingRuleName <String>] [-TableName <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="51b93-111">UpdateExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="51b93-111">UpdateExpandedEventGrid</span></span>
```
Invoke-AzKustoDataConnectionValidation -ConsumerGroup <String> -DataConnectionName <String> -Kind <Kind>
 -Location <String> [-BlobStorageEventType <BlobStorageEventType>] [-DataFormat <EventGridDataFormat>]
 [-IgnoreFirstRecord] [-MappingRuleName <String>] [-TableName <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="51b93-112">UpdateViaIdentityExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="51b93-112">UpdateViaIdentityExpandedEventGrid</span></span>
```
Invoke-AzKustoDataConnectionValidation -ConsumerGroup <String> -DataConnectionName <String> -Kind <Kind>
 -Location <String> [-BlobStorageEventType <BlobStorageEventType>] [-DataFormat <EventGridDataFormat>]
 [-IgnoreFirstRecord] [-MappingRuleName <String>] [-TableName <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="51b93-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="51b93-113">DESCRIPTION</span></span>
<span data-ttu-id="51b93-114">Überprüft, ob die Datenverbindungsparameter gültig sind.</span><span class="sxs-lookup"><span data-stu-id="51b93-114">Checks that the data connection parameters are valid.</span></span>

## <span data-ttu-id="51b93-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="51b93-115">EXAMPLES</span></span>

### <span data-ttu-id="51b93-116">Beispiel 1: Überprüfen von EventHub-Daten Verbindungsparametern</span><span class="sxs-lookup"><span data-stu-id="51b93-116">Example 1: Validate EventHub data connection parameters</span></span>
```powershell
PS C:\> Invoke-AzKustoDataConnectionValidation -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myeventhubdc" -Location "East US" -Kind "EventHub" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -DataFormat "JSON" -ConsumerGroup '$Default' -Compression "None" -TableName "Events" -MappingRuleName "NewEventsMapping"

ErrorMessage
------------
event hub resource id and consumer group tuple provided are already used
```

<span data-ttu-id="51b93-117">Der obige Befehl überprüft die EventHub-Datenverbindung mit dem Namen "myeventhubdc" für die Datenbank "mykustodatabase" im Cluster "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="51b93-117">The above command validates EventHub data connection named "myeventhubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="51b93-118">Beispiel 2: Überprüfen von EventGrid-Daten Verbindungsparametern</span><span class="sxs-lookup"><span data-stu-id="51b93-118">Example 2: Validate EventGrid data connection parameters</span></span>
```powershell
PS C:\> Invoke-AzKustoDataConnectionValidation -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myeventgriddc" -Location "East US" -Kind "EventGrid" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -StorageAccountResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Storage/storageAccounts/mystorage" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "NewEventsMapping"

ErrorMessage
------------
event hub resource id and consumer group tuple provided are already used
```

<span data-ttu-id="51b93-119">Der obige Befehl überprüft die EventGrid-Datenverbindung mit dem Namen "myeventgriddc" für die Datenbank "mykustodatabase" im Cluster "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="51b93-119">The above command validates EventGrid data connection named "myeventgriddc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="51b93-120">Beispiel 3: Überprüfen von IotHub-Daten Verbindungsparametern</span><span class="sxs-lookup"><span data-stu-id="51b93-120">Example 3: Validate IotHub data connection parameters</span></span>
```powershell
PS C:\> Invoke-AzKustoDataConnectionValidation -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myiothubdc" -Location "East US" -Kind "IotHub" -IotHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Devices/IotHubs/myiothub" -SharedAccessPolicyName "myiothubpolicy" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "NewEventsMapping"

ErrorMessage
------------
event hub resource id and consumer group tuple provided are already used
```

<span data-ttu-id="51b93-121">Der obige Befehl überprüft die IotHub-Datenverbindung mit dem Namen "myiothubdc" für die Datenbank "mykustodatabase" im Cluster "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="51b93-121">The above command validates IotHub data connection named "myiothubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="51b93-122">Beispiel 4: Überprüfen von EventHub-Daten Verbindungsparametern über die Identität</span><span class="sxs-lookup"><span data-stu-id="51b93-122">Example 4: Validate EventHub data connection parameters via identity</span></span>
```powershell
PS C:\> $database = Get-AzKustoDatabase -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" 
PS C:\> Invoke-AzKustoDataConnectionValidation -InputObject $database -DataConnectionName "myeventhubdc" -Location "East US" -Kind "EventHub" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -DataFormat "JSON" -ConsumerGroup '$Default' -Compression "None" -TableName "Events" -MappingRuleName "NewEventsMapping"

ErrorMessage
------------
event hub resource id and consumer group tuple provided are already used
```

<span data-ttu-id="51b93-123">Der obige Befehl überprüft die EventHub-Datenverbindung mit dem Namen "myeventhubdc" für die Datenbank "mykustodatabase" im Cluster "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="51b93-123">The above command validates EventHub data connection named "myeventhubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="51b93-124">Beispiel 5: Überprüfen von EventGrid-Daten Verbindungsparametern über die Identität</span><span class="sxs-lookup"><span data-stu-id="51b93-124">Example 5: Validate EventGrid data connection parameters via identity</span></span>
```powershell
PS C:\> $database = Get-AzKustoDatabase -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase"
PS C:\> Invoke-AzKustoDataConnectionValidation -InputObject $database -DataConnectionName "myeventgriddc" -Location "East US" -Kind "EventGrid" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -StorageAccountResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Storage/storageAccounts/mystorage" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "NewEventsMapping"

ErrorMessage
------------
event hub resource id and consumer group tuple provided are already used
```

<span data-ttu-id="51b93-125">Der obige Befehl überprüft die EventGrid-Datenverbindung mit dem Namen "myeventgriddc" für die Datenbank "mykustodatabase" im Cluster "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="51b93-125">The above command validates EventGrid data connection named "myeventgriddc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="51b93-126">Beispiel 6: Überprüfen von IotHub-Daten Verbindungsparametern über die Identität</span><span class="sxs-lookup"><span data-stu-id="51b93-126">Example 6: Validate IotHub data connection parameters via identity</span></span>
```powershell
PS C:\> $database = Get-AzKustoDatabase -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" 
PS C:\> Invoke-AzKustoDataConnectionValidation -InputObject $database -DataConnectionName "myiothubdc" -Location "East US" -Kind "IotHub" -IotHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Devices/IotHubs/myiothub" -SharedAccessPolicyName "myiothubpolicy" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "NewEventsMapping"

ErrorMessage
------------
event hub resource id and consumer group tuple provided are already used
```

<span data-ttu-id="51b93-127">Der obige Befehl überprüft die IotHub-Datenverbindung mit dem Namen "myiothubdc" für die Datenbank "mykustodatabase" im Cluster "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="51b93-127">The above command validates IotHub data connection named "myiothubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

## <span data-ttu-id="51b93-128">Parameter</span><span class="sxs-lookup"><span data-stu-id="51b93-128">PARAMETERS</span></span>

### <span data-ttu-id="51b93-129">-BlobStorageEventType</span><span class="sxs-lookup"><span data-stu-id="51b93-129">-BlobStorageEventType</span></span>
<span data-ttu-id="51b93-130">Der Name des zu verarbeitenden BLOB-Speicherereignis Typs.</span><span class="sxs-lookup"><span data-stu-id="51b93-130">The name of blob storage event type to process.</span></span>

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

### <span data-ttu-id="51b93-131">-Clustername</span><span class="sxs-lookup"><span data-stu-id="51b93-131">-ClusterName</span></span>
<span data-ttu-id="51b93-132">Der Name des Kusto-Clusters.</span><span class="sxs-lookup"><span data-stu-id="51b93-132">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: DataExpandedEventGrid, DataExpandedEventHub, DataExpandedIotHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51b93-133">-Komprimierung</span><span class="sxs-lookup"><span data-stu-id="51b93-133">-Compression</span></span>
<span data-ttu-id="51b93-134">Der Komprimierungstyp des Ereignis-Hub-Nachrichtentyps.</span><span class="sxs-lookup"><span data-stu-id="51b93-134">The event hub messages compression type.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.Compression
Parameter Sets: DataExpandedEventHub, DataViaIdentityExpandedEventHub
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51b93-135">-Consumergroup</span><span class="sxs-lookup"><span data-stu-id="51b93-135">-ConsumerGroup</span></span>
<span data-ttu-id="51b93-136">Die Verbrauchergruppe "Event/viel Hub"</span><span class="sxs-lookup"><span data-stu-id="51b93-136">The event/iot hub consumer group.</span></span>

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

### <span data-ttu-id="51b93-137">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="51b93-137">-DatabaseName</span></span>
<span data-ttu-id="51b93-138">Der Name der Datenbank im Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="51b93-138">The name of the database in the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: DataExpandedEventGrid, DataExpandedEventHub, DataExpandedIotHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51b93-139">-Dataconnectionname</span><span class="sxs-lookup"><span data-stu-id="51b93-139">-DataConnectionName</span></span>
<span data-ttu-id="51b93-140">Der Name der Datenverbindung.</span><span class="sxs-lookup"><span data-stu-id="51b93-140">The name of the data connection.</span></span>

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

### <span data-ttu-id="51b93-141">-DataFormat</span><span class="sxs-lookup"><span data-stu-id="51b93-141">-DataFormat</span></span>
<span data-ttu-id="51b93-142">Das Datenformat der Nachricht.</span><span class="sxs-lookup"><span data-stu-id="51b93-142">The data format of the message.</span></span>
<span data-ttu-id="51b93-143">Optional kann das Datenformat jeder Nachricht hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="51b93-143">Optionally the data format can be added to each message.</span></span>

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

### <span data-ttu-id="51b93-144">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51b93-144">-DefaultProfile</span></span>
<span data-ttu-id="51b93-145">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="51b93-145">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="51b93-146">-EventHubResourceId</span><span class="sxs-lookup"><span data-stu-id="51b93-146">-EventHubResourceId</span></span>
<span data-ttu-id="51b93-147">Die Ressourcen-ID des Ereignis Hubs, der zum Erstellen eines Daten Verbindungs-/Ereignis Rasters verwendet werden soll, ist für das Senden von Ereignissen konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="51b93-147">The resource ID of the event hub to be used to create a data connection / event grid is configured to send events.</span></span>

```yaml
Type: System.String
Parameter Sets: DataExpandedEventGrid, DataExpandedEventHub, DataViaIdentityExpandedEventGrid, DataViaIdentityExpandedEventHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51b93-148">-EventSystemProperty</span><span class="sxs-lookup"><span data-stu-id="51b93-148">-EventSystemProperty</span></span>
<span data-ttu-id="51b93-149">System Eigenschaften des Event/viele-Hubs</span><span class="sxs-lookup"><span data-stu-id="51b93-149">System properties of the event/iot hub.</span></span>

```yaml
Type: System.String[]
Parameter Sets: DataExpandedEventHub, DataExpandedIotHub, DataViaIdentityExpandedEventHub, DataViaIdentityExpandedIotHub
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51b93-150">-IgnoreFirstRecord</span><span class="sxs-lookup"><span data-stu-id="51b93-150">-IgnoreFirstRecord</span></span>
<span data-ttu-id="51b93-151">Ist auf "true" festgelegt, gibt an, dass die Einnahme den ersten Datensatz jeder Datei ignorieren soll.</span><span class="sxs-lookup"><span data-stu-id="51b93-151">If set to true, indicates that ingestion should ignore the first record of every file.</span></span>

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

### <span data-ttu-id="51b93-152">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="51b93-152">-InputObject</span></span>
<span data-ttu-id="51b93-153">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="51b93-153">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: DataViaIdentityExpandedEventGrid, DataViaIdentityExpandedEventHub, DataViaIdentityExpandedIotHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="51b93-154">-IotHubResourceId</span><span class="sxs-lookup"><span data-stu-id="51b93-154">-IotHubResourceId</span></span>
<span data-ttu-id="51b93-155">Die Ressourcen-ID des viel-Hubs, der zum Erstellen einer Datenverbindung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="51b93-155">The resource ID of the Iot hub to be used to create a data connection.</span></span>

```yaml
Type: System.String
Parameter Sets: DataExpandedIotHub, DataViaIdentityExpandedIotHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51b93-156">-Art</span><span class="sxs-lookup"><span data-stu-id="51b93-156">-Kind</span></span>
<span data-ttu-id="51b93-157">Art des Endpunkts für die Datenverbindung</span><span class="sxs-lookup"><span data-stu-id="51b93-157">Kind of the endpoint for the data connection</span></span>

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

### <span data-ttu-id="51b93-158">-Standort</span><span class="sxs-lookup"><span data-stu-id="51b93-158">-Location</span></span>
<span data-ttu-id="51b93-159">Ressourcen Standort.</span><span class="sxs-lookup"><span data-stu-id="51b93-159">Resource location.</span></span>

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

### <span data-ttu-id="51b93-160">-MappingRuleName</span><span class="sxs-lookup"><span data-stu-id="51b93-160">-MappingRuleName</span></span>
<span data-ttu-id="51b93-161">Die Zuordnungsregel, die zum Aufnehmen der Daten verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="51b93-161">The mapping rule to be used to ingest the data.</span></span>
<span data-ttu-id="51b93-162">Optional können die Zuordnungsinformationen jeder Nachricht hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="51b93-162">Optionally the mapping information can be added to each message.</span></span>

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

### <span data-ttu-id="51b93-163">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51b93-163">-ResourceGroupName</span></span>
<span data-ttu-id="51b93-164">Der Name der Ressourcengruppe, die den Kusto-Cluster enthält.</span><span class="sxs-lookup"><span data-stu-id="51b93-164">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: DataExpandedEventGrid, DataExpandedEventHub, DataExpandedIotHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51b93-165">-SharedAccessPolicyName</span><span class="sxs-lookup"><span data-stu-id="51b93-165">-SharedAccessPolicyName</span></span>
<span data-ttu-id="51b93-166">Der Name der Freigabe Zugriffsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="51b93-166">The name of the share access policy.</span></span>

```yaml
Type: System.String
Parameter Sets: DataExpandedIotHub, DataViaIdentityExpandedIotHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51b93-167">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="51b93-167">-StorageAccountResourceId</span></span>
<span data-ttu-id="51b93-168">Die Ressourcen-ID des speicherkontos, in dem sich die Daten befinden.</span><span class="sxs-lookup"><span data-stu-id="51b93-168">The resource ID of the storage account where the data resides.</span></span>

```yaml
Type: System.String
Parameter Sets: DataExpandedEventGrid, DataViaIdentityExpandedEventGrid
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51b93-169">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="51b93-169">-SubscriptionId</span></span>
<span data-ttu-id="51b93-170">Ruft Abonnement Anmeldeinformationen ab, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="51b93-170">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="51b93-171">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="51b93-171">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: DataExpandedEventGrid, DataExpandedEventHub, DataExpandedIotHub
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51b93-172">-Tabellenname</span><span class="sxs-lookup"><span data-stu-id="51b93-172">-TableName</span></span>
<span data-ttu-id="51b93-173">Die Tabelle, in der die Daten aufgenommen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="51b93-173">The table where the data should be ingested.</span></span>
<span data-ttu-id="51b93-174">Optional können die Tabelleninformationen zu den einzelnen Nachrichten hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="51b93-174">Optionally the table information can be added to each message.</span></span>

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

### <span data-ttu-id="51b93-175">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="51b93-175">-Confirm</span></span>
<span data-ttu-id="51b93-176">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="51b93-176">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="51b93-177">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51b93-177">-WhatIf</span></span>
<span data-ttu-id="51b93-178">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="51b93-178">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="51b93-179">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="51b93-179">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="51b93-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51b93-180">CommonParameters</span></span>
<span data-ttu-id="51b93-181">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51b93-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51b93-182">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="51b93-182">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51b93-183">Eingaben</span><span class="sxs-lookup"><span data-stu-id="51b93-183">INPUTS</span></span>

### <span data-ttu-id="51b93-184">Microsoft. Azure. PowerShell. Cmdlets. Kusto. Models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="51b93-184">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="51b93-185">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="51b93-185">OUTPUTS</span></span>

### <span data-ttu-id="51b93-186">Microsoft. Azure. PowerShell. Cmdlets. Kusto. Models. Api20200614. IDataConnectionValidationResult</span><span class="sxs-lookup"><span data-stu-id="51b93-186">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IDataConnectionValidationResult</span></span>

## <span data-ttu-id="51b93-187">Notizen</span><span class="sxs-lookup"><span data-stu-id="51b93-187">NOTES</span></span>

<span data-ttu-id="51b93-188">Aliase</span><span class="sxs-lookup"><span data-stu-id="51b93-188">ALIASES</span></span>

<span data-ttu-id="51b93-189">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="51b93-189">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="51b93-190">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="51b93-190">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="51b93-191">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="51b93-191">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="51b93-192">Inputobject <IKustoIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="51b93-192">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="51b93-193">`[AttachedDatabaseConfigurationName <String>]`: Der Name der angefügten Datenbankkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="51b93-193">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="51b93-194">`[ClusterName <String>]`: Der Name des Kusto-Clusters.</span><span class="sxs-lookup"><span data-stu-id="51b93-194">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="51b93-195">`[DataConnectionName <String>]`: Der Name der Datenverbindung.</span><span class="sxs-lookup"><span data-stu-id="51b93-195">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="51b93-196">`[DatabaseName <String>]`: Der Name der Datenbank im Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="51b93-196">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="51b93-197">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="51b93-197">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="51b93-198">`[Location <String>]`: Azure-Position.</span><span class="sxs-lookup"><span data-stu-id="51b93-198">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="51b93-199">`[PrincipalAssignmentName <String>]`: Der Name des Kusto-principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="51b93-199">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="51b93-200">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die den Kusto-Cluster enthält.</span><span class="sxs-lookup"><span data-stu-id="51b93-200">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="51b93-201">`[SubscriptionId <String>]`: Ruft Abonnement Anmeldeinformationen ab, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="51b93-201">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="51b93-202">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="51b93-202">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="51b93-203">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="51b93-203">RELATED LINKS</span></span>

