---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/invoke-azkustodataconnectionvalidation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Invoke-AzKustoDataConnectionValidation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Invoke-AzKustoDataConnectionValidation.md
ms.openlocfilehash: fa75072cdb29d7aedc7a78ba4e20950b904f1c7f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98472346"
---
# <span data-ttu-id="7f4dc-101">Invoke-AzKustoDataConnectionValidation</span><span class="sxs-lookup"><span data-stu-id="7f4dc-101">Invoke-AzKustoDataConnectionValidation</span></span>

## <span data-ttu-id="7f4dc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7f4dc-102">SYNOPSIS</span></span>
<span data-ttu-id="7f4dc-103">Überprüft, ob die Datenverbindungsparameter gültig sind.</span><span class="sxs-lookup"><span data-stu-id="7f4dc-103">Checks that the data connection parameters are valid.</span></span>

## <span data-ttu-id="7f4dc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7f4dc-104">SYNTAX</span></span>

### <span data-ttu-id="7f4dc-105">DataExpandedEventHub (Standard)</span><span class="sxs-lookup"><span data-stu-id="7f4dc-105">DataExpandedEventHub (Default)</span></span>
```
Invoke-AzKustoDataConnectionValidation -ClusterName <String> -DatabaseName <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -DataConnectionName <String> -EventHubResourceId <String>
 -Kind <Kind> -Location <String> [-SubscriptionId <String>] [-Compression <Compression>]
 [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>] [-MappingRuleName <String>]
 [-TableName <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="7f4dc-106">DataExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="7f4dc-106">DataExpandedEventGrid</span></span>
```
Invoke-AzKustoDataConnectionValidation -ClusterName <String> -DatabaseName <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -DataConnectionName <String> -EventHubResourceId <String>
 -Kind <Kind> -Location <String> -StorageAccountResourceId <String> [-SubscriptionId <String>]
 [-DataFormat <EventGridDataFormat>] [-MappingRuleName <String>] [-TableName <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="7f4dc-107">DataExpandedIotHub</span><span class="sxs-lookup"><span data-stu-id="7f4dc-107">DataExpandedIotHub</span></span>
```
Invoke-AzKustoDataConnectionValidation -ClusterName <String> -DatabaseName <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -DataConnectionName <String> -IotHubResourceId <String>
 -Kind <Kind> -Location <String> -SharedAccessPolicyName <String> [-SubscriptionId <String>]
 [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>] [-MappingRuleName <String>]
 [-TableName <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="7f4dc-108">DataViaIdentityExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="7f4dc-108">DataViaIdentityExpandedEventGrid</span></span>
```
Invoke-AzKustoDataConnectionValidation -InputObject <IKustoIdentity> -ConsumerGroup <String>
 -DataConnectionName <String> -EventHubResourceId <String> -Kind <Kind> -Location <String>
 -StorageAccountResourceId <String> [-DataFormat <EventGridDataFormat>] [-MappingRuleName <String>]
 [-TableName <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="7f4dc-109">DataViaIdentityExpandedEventHub</span><span class="sxs-lookup"><span data-stu-id="7f4dc-109">DataViaIdentityExpandedEventHub</span></span>
```
Invoke-AzKustoDataConnectionValidation -InputObject <IKustoIdentity> -ConsumerGroup <String>
 -DataConnectionName <String> -EventHubResourceId <String> -Kind <Kind> -Location <String>
 [-Compression <Compression>] [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>]
 [-MappingRuleName <String>] [-TableName <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="7f4dc-110">DataViaIdentityExpandedIotHub</span><span class="sxs-lookup"><span data-stu-id="7f4dc-110">DataViaIdentityExpandedIotHub</span></span>
```
Invoke-AzKustoDataConnectionValidation -InputObject <IKustoIdentity> -ConsumerGroup <String>
 -DataConnectionName <String> -IotHubResourceId <String> -Kind <Kind> -Location <String>
 -SharedAccessPolicyName <String> [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>]
 [-MappingRuleName <String>] [-TableName <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="7f4dc-111">UpdateExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="7f4dc-111">UpdateExpandedEventGrid</span></span>
```
Invoke-AzKustoDataConnectionValidation -ConsumerGroup <String> -DataConnectionName <String> -Kind <Kind>
 -Location <String> [-BlobStorageEventType <BlobStorageEventType>] [-DataFormat <EventGridDataFormat>]
 [-IgnoreFirstRecord] [-MappingRuleName <String>] [-TableName <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="7f4dc-112">UpdateViaIdentityExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="7f4dc-112">UpdateViaIdentityExpandedEventGrid</span></span>
```
Invoke-AzKustoDataConnectionValidation -ConsumerGroup <String> -DataConnectionName <String> -Kind <Kind>
 -Location <String> [-BlobStorageEventType <BlobStorageEventType>] [-DataFormat <EventGridDataFormat>]
 [-IgnoreFirstRecord] [-MappingRuleName <String>] [-TableName <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="7f4dc-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7f4dc-113">DESCRIPTION</span></span>
<span data-ttu-id="7f4dc-114">Überprüft, ob die Datenverbindungsparameter gültig sind.</span><span class="sxs-lookup"><span data-stu-id="7f4dc-114">Checks that the data connection parameters are valid.</span></span>

## <span data-ttu-id="7f4dc-115">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="7f4dc-115">EXAMPLES</span></span>

### <span data-ttu-id="7f4dc-116">Beispiel 1: Überprüfen von Parametern für die EreignisHub-Datenverbindung</span><span class="sxs-lookup"><span data-stu-id="7f4dc-116">Example 1: Validate EventHub data connection parameters</span></span>
```powershell
PS C:\> Invoke-AzKustoDataConnectionValidation -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myeventhubdc" -Location "East US" -Kind "EventHub" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -DataFormat "JSON" -ConsumerGroup '$Default' -Compression "None" -TableName "Events" -MappingRuleName "NewEventsMapping"

ErrorMessage
------------
event hub resource id and consumer group tuple provided are already used
```

<span data-ttu-id="7f4dc-117">Mit dem oben angegebenen Befehl wird die EreignisHub-Datenverbindung mit dem Namen "myeventhubdc" für die Datenbank "mykustodatabase" im Cluster "testnewkustocluster" überprüft.</span><span class="sxs-lookup"><span data-stu-id="7f4dc-117">The above command validates EventHub data connection named "myeventhubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="7f4dc-118">Beispiel 2: Überprüfen von Parametern für die EventGrid-Datenverbindung</span><span class="sxs-lookup"><span data-stu-id="7f4dc-118">Example 2: Validate EventGrid data connection parameters</span></span>
```powershell
PS C:\> Invoke-AzKustoDataConnectionValidation -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myeventgriddc" -Location "East US" -Kind "EventGrid" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -StorageAccountResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Storage/storageAccounts/mystorage" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "NewEventsMapping"

ErrorMessage
------------
event hub resource id and consumer group tuple provided are already used
```

<span data-ttu-id="7f4dc-119">Der obige Befehl überprüft die EventGrid-Datenverbindung mit dem Namen "myeventgriddc" für die Datenbank "mykustodatabase" im Cluster "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="7f4dc-119">The above command validates EventGrid data connection named "myeventgriddc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="7f4dc-120">Beispiel 3: Überprüfen von Parametern für die IotHub-Datenverbindung</span><span class="sxs-lookup"><span data-stu-id="7f4dc-120">Example 3: Validate IotHub data connection parameters</span></span>
```powershell
PS C:\> Invoke-AzKustoDataConnectionValidation -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myiothubdc" -Location "East US" -Kind "IotHub" -IotHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Devices/IotHubs/myiothub" -SharedAccessPolicyName "myiothubpolicy" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "NewEventsMapping"

ErrorMessage
------------
event hub resource id and consumer group tuple provided are already used
```

<span data-ttu-id="7f4dc-121">Mit dem vorstehenden Befehl wird die IotHub-Datenverbindung mit dem Namen "myiothubdc" für die Datenbank "mykustodatabase" im Cluster "testnewkustocluster" überprüft.</span><span class="sxs-lookup"><span data-stu-id="7f4dc-121">The above command validates IotHub data connection named "myiothubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="7f4dc-122">Beispiel 4: Überprüfen von Parametern der EreignisHub-Datenverbindung über Identität</span><span class="sxs-lookup"><span data-stu-id="7f4dc-122">Example 4: Validate EventHub data connection parameters via identity</span></span>
```powershell
PS C:\> $database = Get-AzKustoDatabase -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" 
PS C:\> Invoke-AzKustoDataConnectionValidation -InputObject $database -DataConnectionName "myeventhubdc" -Location "East US" -Kind "EventHub" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -DataFormat "JSON" -ConsumerGroup '$Default' -Compression "None" -TableName "Events" -MappingRuleName "NewEventsMapping"

ErrorMessage
------------
event hub resource id and consumer group tuple provided are already used
```

<span data-ttu-id="7f4dc-123">Mit dem oben angegebenen Befehl wird die EreignisHub-Datenverbindung mit dem Namen "myeventhubdc" für die Datenbank "mykustodatabase" im Cluster "testnewkustocluster" überprüft.</span><span class="sxs-lookup"><span data-stu-id="7f4dc-123">The above command validates EventHub data connection named "myeventhubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="7f4dc-124">Beispiel 5: Überprüfen von Parametern der EventGrid-Datenverbindung über Identität</span><span class="sxs-lookup"><span data-stu-id="7f4dc-124">Example 5: Validate EventGrid data connection parameters via identity</span></span>
```powershell
PS C:\> $database = Get-AzKustoDatabase -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase"
PS C:\> Invoke-AzKustoDataConnectionValidation -InputObject $database -DataConnectionName "myeventgriddc" -Location "East US" -Kind "EventGrid" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -StorageAccountResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Storage/storageAccounts/mystorage" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "NewEventsMapping"

ErrorMessage
------------
event hub resource id and consumer group tuple provided are already used
```

<span data-ttu-id="7f4dc-125">Der obige Befehl überprüft die EventGrid-Datenverbindung mit dem Namen "myeventgriddc" für die Datenbank "mykustodatabase" im Cluster "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="7f4dc-125">The above command validates EventGrid data connection named "myeventgriddc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="7f4dc-126">Beispiel 6: Überprüfen von IotHub-Datenverbindungsparametern über Identität</span><span class="sxs-lookup"><span data-stu-id="7f4dc-126">Example 6: Validate IotHub data connection parameters via identity</span></span>
```powershell
PS C:\> $database = Get-AzKustoDatabase -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" 
PS C:\> Invoke-AzKustoDataConnectionValidation -InputObject $database -DataConnectionName "myiothubdc" -Location "East US" -Kind "IotHub" -IotHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Devices/IotHubs/myiothub" -SharedAccessPolicyName "myiothubpolicy" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "NewEventsMapping"

ErrorMessage
------------
event hub resource id and consumer group tuple provided are already used
```

<span data-ttu-id="7f4dc-127">Mit dem vorstehenden Befehl wird die IotHub-Datenverbindung mit dem Namen "myiothubdc" für die Datenbank "mykustodatabase" im Cluster "testnewkustocluster" überprüft.</span><span class="sxs-lookup"><span data-stu-id="7f4dc-127">The above command validates IotHub data connection named "myiothubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

## <span data-ttu-id="7f4dc-128">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7f4dc-128">PARAMETERS</span></span>

### <span data-ttu-id="7f4dc-129">-BlobStorageEventType</span><span class="sxs-lookup"><span data-stu-id="7f4dc-129">-BlobStorageEventType</span></span>
<span data-ttu-id="7f4dc-130">Der Name des zu verarbeitende BLOB-Speicherereignistyps.</span><span class="sxs-lookup"><span data-stu-id="7f4dc-130">The name of blob storage event type to process.</span></span>

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

### <span data-ttu-id="7f4dc-131">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="7f4dc-131">-ClusterName</span></span>
<span data-ttu-id="7f4dc-132">Der Name des Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="7f4dc-132">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="7f4dc-133">-Compression</span><span class="sxs-lookup"><span data-stu-id="7f4dc-133">-Compression</span></span>
<span data-ttu-id="7f4dc-134">Der Komprimierungstyp für Ereignishubnachrichten.</span><span class="sxs-lookup"><span data-stu-id="7f4dc-134">The event hub messages compression type.</span></span>

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

### <span data-ttu-id="7f4dc-135">-ConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="7f4dc-135">-ConsumerGroup</span></span>
<span data-ttu-id="7f4dc-136">Die Consumergruppe "Ereignis/iot-Hub".</span><span class="sxs-lookup"><span data-stu-id="7f4dc-136">The event/iot hub consumer group.</span></span>

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

### <span data-ttu-id="7f4dc-137">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="7f4dc-137">-DatabaseName</span></span>
<span data-ttu-id="7f4dc-138">Der Name der Datenbank im Cluster "Kusto".</span><span class="sxs-lookup"><span data-stu-id="7f4dc-138">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="7f4dc-139">-DataConnectionName</span><span class="sxs-lookup"><span data-stu-id="7f4dc-139">-DataConnectionName</span></span>
<span data-ttu-id="7f4dc-140">Der Name der Datenverbindung.</span><span class="sxs-lookup"><span data-stu-id="7f4dc-140">The name of the data connection.</span></span>

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

### <span data-ttu-id="7f4dc-141">-DataFormat</span><span class="sxs-lookup"><span data-stu-id="7f4dc-141">-DataFormat</span></span>
<span data-ttu-id="7f4dc-142">Das Datenformat der Nachricht.</span><span class="sxs-lookup"><span data-stu-id="7f4dc-142">The data format of the message.</span></span>
<span data-ttu-id="7f4dc-143">Optional kann jeder Nachricht das Datenformat hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="7f4dc-143">Optionally the data format can be added to each message.</span></span>

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

### <span data-ttu-id="7f4dc-144">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f4dc-144">-DefaultProfile</span></span>
<span data-ttu-id="7f4dc-145">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7f4dc-145">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7f4dc-146">-EventHubResourceId</span><span class="sxs-lookup"><span data-stu-id="7f4dc-146">-EventHubResourceId</span></span>
<span data-ttu-id="7f4dc-147">Die Ressourcen-ID des Ereignishubs, der zum Erstellen einer Datenverbindung bzw. eines Ereignisrasters verwendet wird, ist für das Senden von Ereignissen konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="7f4dc-147">The resource ID of the event hub to be used to create a data connection / event grid is configured to send events.</span></span>

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

### <span data-ttu-id="7f4dc-148">-EventSystemProperty</span><span class="sxs-lookup"><span data-stu-id="7f4dc-148">-EventSystemProperty</span></span>
<span data-ttu-id="7f4dc-149">Systemeigenschaften des Ereignis-/iot-Hubs.</span><span class="sxs-lookup"><span data-stu-id="7f4dc-149">System properties of the event/iot hub.</span></span>

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

### <span data-ttu-id="7f4dc-150">-IgnoreFirstRecord</span><span class="sxs-lookup"><span data-stu-id="7f4dc-150">-IgnoreFirstRecord</span></span>
<span data-ttu-id="7f4dc-151">Wenn dies auf "true" festgelegt ist, bedeutet dies, dass die Erfassung den ersten Datensatz jeder Datei ignorieren soll.</span><span class="sxs-lookup"><span data-stu-id="7f4dc-151">If set to true, indicates that ingestion should ignore the first record of every file.</span></span>

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

### <span data-ttu-id="7f4dc-152">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7f4dc-152">-InputObject</span></span>
<span data-ttu-id="7f4dc-153">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="7f4dc-153">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="7f4dc-154">-IotHubResourceId</span><span class="sxs-lookup"><span data-stu-id="7f4dc-154">-IotHubResourceId</span></span>
<span data-ttu-id="7f4dc-155">Die Ressourcen-ID des Iot-Hubs, der zum Erstellen einer Datenverbindung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="7f4dc-155">The resource ID of the Iot hub to be used to create a data connection.</span></span>

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

### <span data-ttu-id="7f4dc-156">-Kind</span><span class="sxs-lookup"><span data-stu-id="7f4dc-156">-Kind</span></span>
<span data-ttu-id="7f4dc-157">Art des Endpunkts für die Datenverbindung</span><span class="sxs-lookup"><span data-stu-id="7f4dc-157">Kind of the endpoint for the data connection</span></span>

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

### <span data-ttu-id="7f4dc-158">-Location</span><span class="sxs-lookup"><span data-stu-id="7f4dc-158">-Location</span></span>
<span data-ttu-id="7f4dc-159">Ressourcenspeicherort.</span><span class="sxs-lookup"><span data-stu-id="7f4dc-159">Resource location.</span></span>

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

### <span data-ttu-id="7f4dc-160">-MappingRuleName</span><span class="sxs-lookup"><span data-stu-id="7f4dc-160">-MappingRuleName</span></span>
<span data-ttu-id="7f4dc-161">Die Zuordnungsregel, die zum Erfassung der Daten verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="7f4dc-161">The mapping rule to be used to ingest the data.</span></span>
<span data-ttu-id="7f4dc-162">Optional können die Zuordnungsinformationen jeder Nachricht hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="7f4dc-162">Optionally the mapping information can be added to each message.</span></span>

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

### <span data-ttu-id="7f4dc-163">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f4dc-163">-ResourceGroupName</span></span>
<span data-ttu-id="7f4dc-164">Der Name der Ressourcengruppe, die den Cluster "Kusto" enthält.</span><span class="sxs-lookup"><span data-stu-id="7f4dc-164">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="7f4dc-165">-SharedAccessPolicyName</span><span class="sxs-lookup"><span data-stu-id="7f4dc-165">-SharedAccessPolicyName</span></span>
<span data-ttu-id="7f4dc-166">Der Name der Freigabezugriffsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="7f4dc-166">The name of the share access policy.</span></span>

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

### <span data-ttu-id="7f4dc-167">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="7f4dc-167">-StorageAccountResourceId</span></span>
<span data-ttu-id="7f4dc-168">Die Ressourcen-ID des Speicherkontos, in dem sich die Daten befinden.</span><span class="sxs-lookup"><span data-stu-id="7f4dc-168">The resource ID of the storage account where the data resides.</span></span>

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

### <span data-ttu-id="7f4dc-169">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7f4dc-169">-SubscriptionId</span></span>
<span data-ttu-id="7f4dc-170">Ruft Abonnementanmeldeinformationen ab, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="7f4dc-170">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="7f4dc-171">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="7f4dc-171">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="7f4dc-172">-TableName</span><span class="sxs-lookup"><span data-stu-id="7f4dc-172">-TableName</span></span>
<span data-ttu-id="7f4dc-173">Die Tabelle, in der die Daten aufgenommen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="7f4dc-173">The table where the data should be ingested.</span></span>
<span data-ttu-id="7f4dc-174">Optional können die Tabelleninformationen jeder Nachricht hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="7f4dc-174">Optionally the table information can be added to each message.</span></span>

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

### <span data-ttu-id="7f4dc-175">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7f4dc-175">-Confirm</span></span>
<span data-ttu-id="7f4dc-176">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7f4dc-176">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f4dc-177">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="7f4dc-177">-WhatIf</span></span>
<span data-ttu-id="7f4dc-178">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7f4dc-178">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7f4dc-179">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7f4dc-179">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f4dc-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f4dc-180">CommonParameters</span></span>
<span data-ttu-id="7f4dc-181">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f4dc-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f4dc-182">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7f4dc-182">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f4dc-183">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="7f4dc-183">INPUTS</span></span>

### <span data-ttu-id="7f4dc-184">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="7f4dc-184">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="7f4dc-185">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="7f4dc-185">OUTPUTS</span></span>

### <span data-ttu-id="7f4dc-186">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDataConnectionValidationResult</span><span class="sxs-lookup"><span data-stu-id="7f4dc-186">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDataConnectionValidationResult</span></span>

## <span data-ttu-id="7f4dc-187">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="7f4dc-187">NOTES</span></span>

<span data-ttu-id="7f4dc-188">ALIASE</span><span class="sxs-lookup"><span data-stu-id="7f4dc-188">ALIASES</span></span>

<span data-ttu-id="7f4dc-189">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="7f4dc-189">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="7f4dc-190">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="7f4dc-190">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7f4dc-191">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="7f4dc-191">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="7f4dc-192">INPUTOBJECT <IKustoIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="7f4dc-192">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="7f4dc-193">`[AttachedDatabaseConfigurationName <String>]`: Der Name der angefügten Datenbankkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="7f4dc-193">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="7f4dc-194">`[ClusterName <String>]`: Der Name des Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="7f4dc-194">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="7f4dc-195">`[DataConnectionName <String>]`: Der Name der Datenverbindung.</span><span class="sxs-lookup"><span data-stu-id="7f4dc-195">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="7f4dc-196">`[DatabaseName <String>]`: Der Name der Datenbank im Cluster "Kusto".</span><span class="sxs-lookup"><span data-stu-id="7f4dc-196">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="7f4dc-197">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="7f4dc-197">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="7f4dc-198">`[Location <String>]`: Azure-Standort.</span><span class="sxs-lookup"><span data-stu-id="7f4dc-198">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="7f4dc-199">`[PrincipalAssignmentName <String>]`: Der Name der Kusto PrincipalAssignment.</span><span class="sxs-lookup"><span data-stu-id="7f4dc-199">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="7f4dc-200">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die den Cluster "Kusto" enthält.</span><span class="sxs-lookup"><span data-stu-id="7f4dc-200">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="7f4dc-201">`[SubscriptionId <String>]`: Ruft Abonnementanmeldeinformationen ab, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="7f4dc-201">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="7f4dc-202">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="7f4dc-202">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="7f4dc-203">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="7f4dc-203">RELATED LINKS</span></span>

