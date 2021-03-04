---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/invoke-azkustodataconnectionvalidation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Invoke-AzKustoDataConnectionValidation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Invoke-AzKustoDataConnectionValidation.md
ms.openlocfilehash: c12c38227c4d0a3d0a6b58685c1b8b5233c161ad
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101922427"
---
# <span data-ttu-id="d803b-101">Invoke-AzKustoDataConnectionValidation</span><span class="sxs-lookup"><span data-stu-id="d803b-101">Invoke-AzKustoDataConnectionValidation</span></span>

## <span data-ttu-id="d803b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d803b-102">SYNOPSIS</span></span>
<span data-ttu-id="d803b-103">Überprüft, ob die Datenverbindungsparameter gültig sind.</span><span class="sxs-lookup"><span data-stu-id="d803b-103">Checks that the data connection parameters are valid.</span></span>

## <span data-ttu-id="d803b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d803b-104">SYNTAX</span></span>

### <span data-ttu-id="d803b-105">DataExpandedEventHub (Standard)</span><span class="sxs-lookup"><span data-stu-id="d803b-105">DataExpandedEventHub (Default)</span></span>
```
Invoke-AzKustoDataConnectionValidation -ClusterName <String> -DatabaseName <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -DataConnectionName <String> -EventHubResourceId <String>
 -Kind <Kind> -Location <String> [-SubscriptionId <String>] [-Compression <Compression>]
 [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>] [-MappingRuleName <String>]
 [-TableName <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d803b-106">DataExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="d803b-106">DataExpandedEventGrid</span></span>
```
Invoke-AzKustoDataConnectionValidation -ClusterName <String> -DatabaseName <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -DataConnectionName <String> -EventHubResourceId <String>
 -Kind <Kind> -Location <String> -StorageAccountResourceId <String> [-SubscriptionId <String>]
 [-DataFormat <EventGridDataFormat>] [-MappingRuleName <String>] [-TableName <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d803b-107">DataExpandedIotHub</span><span class="sxs-lookup"><span data-stu-id="d803b-107">DataExpandedIotHub</span></span>
```
Invoke-AzKustoDataConnectionValidation -ClusterName <String> -DatabaseName <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -DataConnectionName <String> -IotHubResourceId <String>
 -Kind <Kind> -Location <String> -SharedAccessPolicyName <String> [-SubscriptionId <String>]
 [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>] [-MappingRuleName <String>]
 [-TableName <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d803b-108">DataViaIdentityExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="d803b-108">DataViaIdentityExpandedEventGrid</span></span>
```
Invoke-AzKustoDataConnectionValidation -InputObject <IKustoIdentity> -ConsumerGroup <String>
 -DataConnectionName <String> -EventHubResourceId <String> -Kind <Kind> -Location <String>
 -StorageAccountResourceId <String> [-DataFormat <EventGridDataFormat>] [-MappingRuleName <String>]
 [-TableName <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d803b-109">DataViaIdentityExpandedEventHub</span><span class="sxs-lookup"><span data-stu-id="d803b-109">DataViaIdentityExpandedEventHub</span></span>
```
Invoke-AzKustoDataConnectionValidation -InputObject <IKustoIdentity> -ConsumerGroup <String>
 -DataConnectionName <String> -EventHubResourceId <String> -Kind <Kind> -Location <String>
 [-Compression <Compression>] [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>]
 [-MappingRuleName <String>] [-TableName <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="d803b-110">DataViaIdentityExpandedIotHub</span><span class="sxs-lookup"><span data-stu-id="d803b-110">DataViaIdentityExpandedIotHub</span></span>
```
Invoke-AzKustoDataConnectionValidation -InputObject <IKustoIdentity> -ConsumerGroup <String>
 -DataConnectionName <String> -IotHubResourceId <String> -Kind <Kind> -Location <String>
 -SharedAccessPolicyName <String> [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>]
 [-MappingRuleName <String>] [-TableName <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="d803b-111">UpdateExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="d803b-111">UpdateExpandedEventGrid</span></span>
```
Invoke-AzKustoDataConnectionValidation -ConsumerGroup <String> -DataConnectionName <String> -Kind <Kind>
 -Location <String> [-BlobStorageEventType <BlobStorageEventType>] [-DataFormat <EventGridDataFormat>]
 [-IgnoreFirstRecord] [-MappingRuleName <String>] [-TableName <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d803b-112">UpdateViaIdentityExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="d803b-112">UpdateViaIdentityExpandedEventGrid</span></span>
```
Invoke-AzKustoDataConnectionValidation -ConsumerGroup <String> -DataConnectionName <String> -Kind <Kind>
 -Location <String> [-BlobStorageEventType <BlobStorageEventType>] [-DataFormat <EventGridDataFormat>]
 [-IgnoreFirstRecord] [-MappingRuleName <String>] [-TableName <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d803b-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d803b-113">DESCRIPTION</span></span>
<span data-ttu-id="d803b-114">Überprüft, ob die Datenverbindungsparameter gültig sind.</span><span class="sxs-lookup"><span data-stu-id="d803b-114">Checks that the data connection parameters are valid.</span></span>

## <span data-ttu-id="d803b-115">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d803b-115">EXAMPLES</span></span>

### <span data-ttu-id="d803b-116">Beispiel 1: Überprüfen von Parametern für die EreignisHub-Datenverbindung</span><span class="sxs-lookup"><span data-stu-id="d803b-116">Example 1: Validate EventHub data connection parameters</span></span>
```powershell
PS C:\> Invoke-AzKustoDataConnectionValidation -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myeventhubdc" -Location "East US" -Kind "EventHub" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -DataFormat "JSON" -ConsumerGroup '$Default' -Compression "None" -TableName "Events" -MappingRuleName "NewEventsMapping"

ErrorMessage
------------
event hub resource id and consumer group tuple provided are already used
```

<span data-ttu-id="d803b-117">Der obige Befehl überprüft die EreignisHub-Datenverbindung mit dem Namen "myeventhubdc" für die Datenbank "mykustodatabase" im Cluster "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="d803b-117">The above command validates EventHub data connection named "myeventhubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="d803b-118">Beispiel 2: Überprüfen von Parametern für die EventGrid-Datenverbindung</span><span class="sxs-lookup"><span data-stu-id="d803b-118">Example 2: Validate EventGrid data connection parameters</span></span>
```powershell
PS C:\> Invoke-AzKustoDataConnectionValidation -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myeventgriddc" -Location "East US" -Kind "EventGrid" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -StorageAccountResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Storage/storageAccounts/mystorage" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "NewEventsMapping"

ErrorMessage
------------
event hub resource id and consumer group tuple provided are already used
```

<span data-ttu-id="d803b-119">Der obige Befehl überprüft die EreignisGrid-Datenverbindung mit dem Namen "myeventgriddc" für die Datenbank "mykustodatabase" im Cluster "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="d803b-119">The above command validates EventGrid data connection named "myeventgriddc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="d803b-120">Beispiel 3: Überprüfen von IotHub-Datenverbindungsparametern</span><span class="sxs-lookup"><span data-stu-id="d803b-120">Example 3: Validate IotHub data connection parameters</span></span>
```powershell
PS C:\> Invoke-AzKustoDataConnectionValidation -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myiothubdc" -Location "East US" -Kind "IotHub" -IotHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Devices/IotHubs/myiothub" -SharedAccessPolicyName "myiothubpolicy" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "NewEventsMapping"

ErrorMessage
------------
event hub resource id and consumer group tuple provided are already used
```

<span data-ttu-id="d803b-121">Der obige Befehl überprüft die IotHub-Datenverbindung mit dem Namen "myiothubdc" für die Datenbank "mykustodatabase" im Cluster "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="d803b-121">The above command validates IotHub data connection named "myiothubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="d803b-122">Beispiel 4: Überprüfen von Parametern für die Ereignishub-Datenverbindung über die Identität</span><span class="sxs-lookup"><span data-stu-id="d803b-122">Example 4: Validate EventHub data connection parameters via identity</span></span>
```powershell
PS C:\> $database = Get-AzKustoDatabase -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" 
PS C:\> Invoke-AzKustoDataConnectionValidation -InputObject $database -DataConnectionName "myeventhubdc" -Location "East US" -Kind "EventHub" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -DataFormat "JSON" -ConsumerGroup '$Default' -Compression "None" -TableName "Events" -MappingRuleName "NewEventsMapping"

ErrorMessage
------------
event hub resource id and consumer group tuple provided are already used
```

<span data-ttu-id="d803b-123">Der obige Befehl überprüft die EreignisHub-Datenverbindung mit dem Namen "myeventhubdc" für die Datenbank "mykustodatabase" im Cluster "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="d803b-123">The above command validates EventHub data connection named "myeventhubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="d803b-124">Beispiel 5: Überprüfen von Parametern der EventGrid-Datenverbindung über die Identität</span><span class="sxs-lookup"><span data-stu-id="d803b-124">Example 5: Validate EventGrid data connection parameters via identity</span></span>
```powershell
PS C:\> $database = Get-AzKustoDatabase -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase"
PS C:\> Invoke-AzKustoDataConnectionValidation -InputObject $database -DataConnectionName "myeventgriddc" -Location "East US" -Kind "EventGrid" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -StorageAccountResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Storage/storageAccounts/mystorage" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "NewEventsMapping"

ErrorMessage
------------
event hub resource id and consumer group tuple provided are already used
```

<span data-ttu-id="d803b-125">Der obige Befehl überprüft die EreignisGrid-Datenverbindung mit dem Namen "myeventgriddc" für die Datenbank "mykustodatabase" im Cluster "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="d803b-125">The above command validates EventGrid data connection named "myeventgriddc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="d803b-126">Beispiel 6: Überprüfen von IotHub-Datenverbindungsparametern über die Identität</span><span class="sxs-lookup"><span data-stu-id="d803b-126">Example 6: Validate IotHub data connection parameters via identity</span></span>
```powershell
PS C:\> $database = Get-AzKustoDatabase -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" 
PS C:\> Invoke-AzKustoDataConnectionValidation -InputObject $database -DataConnectionName "myiothubdc" -Location "East US" -Kind "IotHub" -IotHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Devices/IotHubs/myiothub" -SharedAccessPolicyName "myiothubpolicy" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "NewEventsMapping"

ErrorMessage
------------
event hub resource id and consumer group tuple provided are already used
```

<span data-ttu-id="d803b-127">Der obige Befehl überprüft die IotHub-Datenverbindung mit dem Namen "myiothubdc" für die Datenbank "mykustodatabase" im Cluster "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="d803b-127">The above command validates IotHub data connection named "myiothubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

## <span data-ttu-id="d803b-128">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="d803b-128">PARAMETERS</span></span>

### <span data-ttu-id="d803b-129">-BlobStorageEventType</span><span class="sxs-lookup"><span data-stu-id="d803b-129">-BlobStorageEventType</span></span>
<span data-ttu-id="d803b-130">Der Name des zu verarbeitende Blobspeicherereignistyps.</span><span class="sxs-lookup"><span data-stu-id="d803b-130">The name of blob storage event type to process.</span></span>

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

### <span data-ttu-id="d803b-131">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="d803b-131">-ClusterName</span></span>
<span data-ttu-id="d803b-132">Der Name des Kusto-Clusters.</span><span class="sxs-lookup"><span data-stu-id="d803b-132">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="d803b-133">-Compression</span><span class="sxs-lookup"><span data-stu-id="d803b-133">-Compression</span></span>
<span data-ttu-id="d803b-134">Der Komprimierungstyp für Ereignishubnachrichten.</span><span class="sxs-lookup"><span data-stu-id="d803b-134">The event hub messages compression type.</span></span>

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

### <span data-ttu-id="d803b-135">-ConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="d803b-135">-ConsumerGroup</span></span>
<span data-ttu-id="d803b-136">Die Ereignis-/iot-Hub-Consumergruppe.</span><span class="sxs-lookup"><span data-stu-id="d803b-136">The event/iot hub consumer group.</span></span>

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

### <span data-ttu-id="d803b-137">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d803b-137">-DatabaseName</span></span>
<span data-ttu-id="d803b-138">Der Name der Datenbank im Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="d803b-138">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="d803b-139">-DataConnectionName</span><span class="sxs-lookup"><span data-stu-id="d803b-139">-DataConnectionName</span></span>
<span data-ttu-id="d803b-140">Der Name der Datenverbindung.</span><span class="sxs-lookup"><span data-stu-id="d803b-140">The name of the data connection.</span></span>

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

### <span data-ttu-id="d803b-141">-DataFormat</span><span class="sxs-lookup"><span data-stu-id="d803b-141">-DataFormat</span></span>
<span data-ttu-id="d803b-142">Das Datenformat der Nachricht.</span><span class="sxs-lookup"><span data-stu-id="d803b-142">The data format of the message.</span></span>
<span data-ttu-id="d803b-143">Optional kann jeder Nachricht das Datenformat hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="d803b-143">Optionally the data format can be added to each message.</span></span>

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

### <span data-ttu-id="d803b-144">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d803b-144">-DefaultProfile</span></span>
<span data-ttu-id="d803b-145">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d803b-145">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d803b-146">-EventHubResourceId</span><span class="sxs-lookup"><span data-stu-id="d803b-146">-EventHubResourceId</span></span>
<span data-ttu-id="d803b-147">Die Ressourcen-ID des Ereignishubs, der zum Erstellen einer Datenverbindung/eines Ereignisrasters verwendet werden soll, ist für das Senden von Ereignissen konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="d803b-147">The resource ID of the event hub to be used to create a data connection / event grid is configured to send events.</span></span>

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

### <span data-ttu-id="d803b-148">-EventSystemProperty</span><span class="sxs-lookup"><span data-stu-id="d803b-148">-EventSystemProperty</span></span>
<span data-ttu-id="d803b-149">Systemeigenschaften des Ereignisses/iot-Hubs.</span><span class="sxs-lookup"><span data-stu-id="d803b-149">System properties of the event/iot hub.</span></span>

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

### <span data-ttu-id="d803b-150">-IgnoreFirstRecord</span><span class="sxs-lookup"><span data-stu-id="d803b-150">-IgnoreFirstRecord</span></span>
<span data-ttu-id="d803b-151">Wenn auf "true" festgelegt ist, gibt an, dass bei der Aufnahme der erste Datensatz jeder Datei ignoriert werden soll.</span><span class="sxs-lookup"><span data-stu-id="d803b-151">If set to true, indicates that ingestion should ignore the first record of every file.</span></span>

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

### <span data-ttu-id="d803b-152">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d803b-152">-InputObject</span></span>
<span data-ttu-id="d803b-153">Identitätsparameter Zum Erstellen lesen Sie den Abschnitt NOTIZEN für INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="d803b-153">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="d803b-154">-IotHubResourceId</span><span class="sxs-lookup"><span data-stu-id="d803b-154">-IotHubResourceId</span></span>
<span data-ttu-id="d803b-155">Die Ressourcen-ID des Iot-Hubs, der zum Erstellen einer Datenverbindung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d803b-155">The resource ID of the Iot hub to be used to create a data connection.</span></span>

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

### <span data-ttu-id="d803b-156">-Kind</span><span class="sxs-lookup"><span data-stu-id="d803b-156">-Kind</span></span>
<span data-ttu-id="d803b-157">Art des Endpunkts für die Datenverbindung</span><span class="sxs-lookup"><span data-stu-id="d803b-157">Kind of the endpoint for the data connection</span></span>

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

### <span data-ttu-id="d803b-158">-Location</span><span class="sxs-lookup"><span data-stu-id="d803b-158">-Location</span></span>
<span data-ttu-id="d803b-159">Ressourcenspeicherort.</span><span class="sxs-lookup"><span data-stu-id="d803b-159">Resource location.</span></span>

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

### <span data-ttu-id="d803b-160">-MappingRuleName</span><span class="sxs-lookup"><span data-stu-id="d803b-160">-MappingRuleName</span></span>
<span data-ttu-id="d803b-161">Die Zuordnungsregel, mit der die Daten aufgenommen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d803b-161">The mapping rule to be used to ingest the data.</span></span>
<span data-ttu-id="d803b-162">Optional können die Zuordnungsinformationen jeder Nachricht hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="d803b-162">Optionally the mapping information can be added to each message.</span></span>

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

### <span data-ttu-id="d803b-163">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d803b-163">-ResourceGroupName</span></span>
<span data-ttu-id="d803b-164">Der Name der Ressourcengruppe, die den Kusto-Cluster enthält.</span><span class="sxs-lookup"><span data-stu-id="d803b-164">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="d803b-165">-SharedAccessPolicyName</span><span class="sxs-lookup"><span data-stu-id="d803b-165">-SharedAccessPolicyName</span></span>
<span data-ttu-id="d803b-166">Der Name der Freigabezugriffsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="d803b-166">The name of the share access policy.</span></span>

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

### <span data-ttu-id="d803b-167">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="d803b-167">-StorageAccountResourceId</span></span>
<span data-ttu-id="d803b-168">Die Ressourcen-ID des Speicherkontos, in dem sich die Daten befinden.</span><span class="sxs-lookup"><span data-stu-id="d803b-168">The resource ID of the storage account where the data resides.</span></span>

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

### <span data-ttu-id="d803b-169">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d803b-169">-SubscriptionId</span></span>
<span data-ttu-id="d803b-170">Ruft Abonnementanmeldeinformationen ab, mit denen Microsoft Azure-Abonnement eindeutig identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="d803b-170">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="d803b-171">Die Abonnement-ID ist Teil des URI für jeden Dienstanruf.</span><span class="sxs-lookup"><span data-stu-id="d803b-171">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="d803b-172">-TableName</span><span class="sxs-lookup"><span data-stu-id="d803b-172">-TableName</span></span>
<span data-ttu-id="d803b-173">Die Tabelle, in der die Daten aufgenommen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d803b-173">The table where the data should be ingested.</span></span>
<span data-ttu-id="d803b-174">Optional können die Tabelleninformationen jeder Nachricht hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="d803b-174">Optionally the table information can be added to each message.</span></span>

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

### <span data-ttu-id="d803b-175">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d803b-175">-Confirm</span></span>
<span data-ttu-id="d803b-176">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d803b-176">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d803b-177">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d803b-177">-WhatIf</span></span>
<span data-ttu-id="d803b-178">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d803b-178">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d803b-179">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d803b-179">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d803b-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d803b-180">CommonParameters</span></span>
<span data-ttu-id="d803b-181">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d803b-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d803b-182">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d803b-182">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d803b-183">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d803b-183">INPUTS</span></span>

### <span data-ttu-id="d803b-184">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="d803b-184">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="d803b-185">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d803b-185">OUTPUTS</span></span>

### <span data-ttu-id="d803b-186">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDataConnectionValidationResult</span><span class="sxs-lookup"><span data-stu-id="d803b-186">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDataConnectionValidationResult</span></span>

## <span data-ttu-id="d803b-187">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="d803b-187">NOTES</span></span>

<span data-ttu-id="d803b-188">ALIASE</span><span class="sxs-lookup"><span data-stu-id="d803b-188">ALIASES</span></span>

<span data-ttu-id="d803b-189">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="d803b-189">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d803b-190">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="d803b-190">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d803b-191">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d803b-191">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d803b-192">INPUTOBJECT <IKustoIdentity> : Identitätsparameter</span><span class="sxs-lookup"><span data-stu-id="d803b-192">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d803b-193">`[AttachedDatabaseConfigurationName <String>]`: Der Name der angefügten Datenbankkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="d803b-193">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="d803b-194">`[ClusterName <String>]`: Der Name des Kusto-Clusters.</span><span class="sxs-lookup"><span data-stu-id="d803b-194">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="d803b-195">`[DataConnectionName <String>]`: Der Name der Datenverbindung.</span><span class="sxs-lookup"><span data-stu-id="d803b-195">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="d803b-196">`[DatabaseName <String>]`: Der Name der Datenbank im Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="d803b-196">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="d803b-197">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="d803b-197">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d803b-198">`[Location <String>]`: Azure-Standort.</span><span class="sxs-lookup"><span data-stu-id="d803b-198">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="d803b-199">`[PrincipalAssignmentName <String>]`: Der Name der Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="d803b-199">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="d803b-200">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die den Kusto-Cluster enthält.</span><span class="sxs-lookup"><span data-stu-id="d803b-200">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="d803b-201">`[SubscriptionId <String>]`: Ruft Abonnementanmeldeinformationen ab, mit denen Microsoft Azure-Abonnement eindeutig identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="d803b-201">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="d803b-202">Die Abonnement-ID ist Teil des URI für jeden Dienstanruf.</span><span class="sxs-lookup"><span data-stu-id="d803b-202">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="d803b-203">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="d803b-203">RELATED LINKS</span></span>

