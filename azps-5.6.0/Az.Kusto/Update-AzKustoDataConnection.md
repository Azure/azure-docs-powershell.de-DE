---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/update-azkustodataconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Update-AzKustoDataConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Update-AzKustoDataConnection.md
ms.openlocfilehash: 94a0764b61b32ce55ff4d9aca06a22d67b1edc96
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101947107"
---
# <span data-ttu-id="eba54-101">Update-AzKustoDataConnection</span><span class="sxs-lookup"><span data-stu-id="eba54-101">Update-AzKustoDataConnection</span></span>

## <span data-ttu-id="eba54-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eba54-102">SYNOPSIS</span></span>
<span data-ttu-id="eba54-103">Aktualisiert eine Datenverbindung.</span><span class="sxs-lookup"><span data-stu-id="eba54-103">Updates a data connection.</span></span>

## <span data-ttu-id="eba54-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="eba54-104">SYNTAX</span></span>

### <span data-ttu-id="eba54-105">UpdateExpandedEventHub (Standard)</span><span class="sxs-lookup"><span data-stu-id="eba54-105">UpdateExpandedEventHub (Default)</span></span>
```
Update-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -EventHubResourceId <String> -Kind <Kind>
 -Location <String> [-SubscriptionId <String>] [-Compression <Compression>]
 [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>] [-MappingRuleName <String>]
 [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="eba54-106">UpdateExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="eba54-106">UpdateExpandedEventGrid</span></span>
```
Update-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -EventHubResourceId <String> -Kind <Kind>
 -Location <String> -StorageAccountResourceId <String> [-SubscriptionId <String>]
 [-BlobStorageEventType <BlobStorageEventType>] [-DataFormat <EventGridDataFormat>] [-IgnoreFirstRecord]
 [-MappingRuleName <String>] [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="eba54-107">UpdateExpandedIotHub</span><span class="sxs-lookup"><span data-stu-id="eba54-107">UpdateExpandedIotHub</span></span>
```
Update-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -IotHubResourceId <String> -Kind <Kind>
 -Location <String> -SharedAccessPolicyName <String> [-SubscriptionId <String>]
 [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>] [-MappingRuleName <String>]
 [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="eba54-108">UpdateViaIdentityExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="eba54-108">UpdateViaIdentityExpandedEventGrid</span></span>
```
Update-AzKustoDataConnection -InputObject <IKustoIdentity> -ConsumerGroup <String>
 -EventHubResourceId <String> -Kind <Kind> -Location <String> -StorageAccountResourceId <String>
 [-BlobStorageEventType <BlobStorageEventType>] [-DataFormat <EventGridDataFormat>] [-IgnoreFirstRecord]
 [-MappingRuleName <String>] [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="eba54-109">UpdateViaIdentityExpandedEventHub</span><span class="sxs-lookup"><span data-stu-id="eba54-109">UpdateViaIdentityExpandedEventHub</span></span>
```
Update-AzKustoDataConnection -InputObject <IKustoIdentity> -ConsumerGroup <String>
 -EventHubResourceId <String> -Kind <Kind> -Location <String> [-Compression <Compression>]
 [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>] [-MappingRuleName <String>]
 [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="eba54-110">UpdateViaIdentityExpandedIotHub</span><span class="sxs-lookup"><span data-stu-id="eba54-110">UpdateViaIdentityExpandedIotHub</span></span>
```
Update-AzKustoDataConnection -InputObject <IKustoIdentity> -ConsumerGroup <String> -IotHubResourceId <String>
 -Kind <Kind> -Location <String> -SharedAccessPolicyName <String> [-DataFormat <EventGridDataFormat>]
 [-EventSystemProperty <String[]>] [-MappingRuleName <String>] [-TableName <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="eba54-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="eba54-111">DESCRIPTION</span></span>
<span data-ttu-id="eba54-112">Aktualisiert eine Datenverbindung.</span><span class="sxs-lookup"><span data-stu-id="eba54-112">Updates a data connection.</span></span>

## <span data-ttu-id="eba54-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="eba54-113">EXAMPLES</span></span>

### <span data-ttu-id="eba54-114">Beispiel 1: Aktualisieren einer vorhandenen EventHub-Datenverbindung</span><span class="sxs-lookup"><span data-stu-id="eba54-114">Example 1: Update an existing EventHub data connection</span></span>
```powershell
PS C:\> Update-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myeventhubdc" -Location="East US" -Kind "EventHub" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -DataFormat "JSON" -ConsumerGroup '$Default' -Compression "None" -TableName "Events" -MappingRuleName "NewEventsMapping"

Kind     Location Name                                             Type
----     -------- ----                                             ----
EventHub East US  testnewkustocluster/mykustodatabase/myeventhubdc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="eba54-115">Der obige Befehl aktualisiert die vorhandene EventHub-Datenverbindung mit dem Namen "myeventhubdc" für die Datenbank "mykustodatabase" im Cluster "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="eba54-115">The above command updates the existing EventHub data connection named "myeventhubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="eba54-116">Beispiel 2: Aktualisieren einer vorhandenen EventGrid-Datenverbindung</span><span class="sxs-lookup"><span data-stu-id="eba54-116">Example 2: Update an existing EventGrid data connection</span></span>
```powershell
PS C:\> Update-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myeventgriddc" -Location="East US" -Kind "EventGrid" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -StorageAccountResourceId $storageAccountResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Storage/storageAccounts/mystorage" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "NewEventsMapping"

Kind      Location Name                                              Type
----      -------- ----                                              ----
EventGrid East US  testnewkustocluster/mykustodatabase/myeventgriddc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="eba54-117">Der obige Befehl aktualisiert die vorhandene EventGrid-Datenverbindung mit dem Namen "myeventgriddc" für die Datenbank "mykustodatabase" im Cluster "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="eba54-117">The above command updates the existing EventGrid data connection named "myeventgriddc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="eba54-118">Beispiel 3: Aktualisieren einer vorhandenen IotHub-Datenverbindung</span><span class="sxs-lookup"><span data-stu-id="eba54-118">Example 3: Update an existing IotHub data connection</span></span>
```powershell
PS C:\> Update-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myiothubdc" -Location="East US" -Kind "IotHub" -IotHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Devices/IotHubs/myiothub" -SharedAccessPolicyName "myiothubpolicy" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "NewEventsMapping"

Kind      Location Name                                        Type
----      -------- ----                                        ----
IotHub East US  testnewkustocluster/mykustodatabase/myiothubdc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="eba54-119">Der obige Befehl aktualisiert die vorhandene IotHub-Datenverbindung mit dem Namen "myiothubdc" für die Datenbank "mykustodatabase" im Cluster "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="eba54-119">The above command updates the existing IotHub data connection named "myiothubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="eba54-120">Beispiel 4: Aktualisieren einer vorhandenen EventHub-Datenverbindung über die Identität</span><span class="sxs-lookup"><span data-stu-id="eba54-120">Example 4: Update an existing EventHub data connection via identity</span></span>
```powershell
PS C:\> $dataConnection = Get-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myeventhubdc" 
PS C:\> Update-AzKustoDataConnection -InputObject $dataConnection -Location="East US" -Kind "EventHub" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -DataFormat "JSON" -ConsumerGroup '$Default' -Compression "None" -TableName "Events" -MappingRuleName "NewEventsMapping"

Kind     Location Name                                             Type
----     -------- ----                                             ----
EventHub East US  testnewkustocluster/mykustodatabase/myeventhubdc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="eba54-121">Der obige Befehl aktualisiert die vorhandene EventHub-Datenverbindung mit dem Namen "myeventhubdc" für die Datenbank "mykustodatabase" im Cluster "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="eba54-121">The above command updates the existing EventHub data connection named "myeventhubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="eba54-122">Beispiel 5: Aktualisieren einer vorhandenen EventGrid-Datenverbindung über die Identität</span><span class="sxs-lookup"><span data-stu-id="eba54-122">Example 5: Update an existing EventGrid data connection via identity</span></span>
```powershell
PS C:\> $dataConnection = Get-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myeventgriddc" 
PS C:\> Update-AzKustoDataConnection -InputObject $dataConnection -Location="East US" -Kind "EventGrid" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -StorageAccountResourceId $storageAccountResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Storage/storageAccounts/mystorage" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "NewEventsMapping"

Kind      Location Name                                              Type
----      -------- ----                                              ----
EventGrid East US  testnewkustocluster/mykustodatabase/myeventgriddc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="eba54-123">Der obige Befehl aktualisiert die vorhandene EventGrid-Datenverbindung mit dem Namen "myeventgriddc" für die Datenbank "mykustodatabase" im Cluster "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="eba54-123">The above command updates the existing EventGrid data connection named "myeventgriddc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="eba54-124">Beispiel 6: Aktualisieren einer vorhandenen IotHub-Datenverbindung über die Identität</span><span class="sxs-lookup"><span data-stu-id="eba54-124">Example 6: Update an existing IotHub data connection via identity</span></span>
```powershell
PS C:\> $dataConnection = Get-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myiothubdc" 
PS C:\> Update-AzKustoDataConnection -InputObject $dataConnection -Location="East US" -Kind "IotHub" -IotHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Devices/IotHubs/myiothub" -SharedAccessPolicyName "myiothubpolicy" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "NewEventsMapping"

Kind      Location Name                                        Type
----      -------- ----                                        ----
IotHub East US  testnewkustocluster/mykustodatabase/myiothubdc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="eba54-125">Der obige Befehl aktualisiert die vorhandene IotHub-Datenverbindung mit dem Namen "myiothubdc" für die Datenbank "mykustodatabase" im Cluster "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="eba54-125">The above command updates the existing IotHub data connection named "myiothubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

## <span data-ttu-id="eba54-126">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="eba54-126">PARAMETERS</span></span>

### <span data-ttu-id="eba54-127">-AsJob</span><span class="sxs-lookup"><span data-stu-id="eba54-127">-AsJob</span></span>
<span data-ttu-id="eba54-128">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="eba54-128">Run the command as a job</span></span>

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

### <span data-ttu-id="eba54-129">-BlobStorageEventType</span><span class="sxs-lookup"><span data-stu-id="eba54-129">-BlobStorageEventType</span></span>
<span data-ttu-id="eba54-130">Der Name des zu verarbeitende Blobspeicherereignistyps.</span><span class="sxs-lookup"><span data-stu-id="eba54-130">The name of blob storage event type to process.</span></span>

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

### <span data-ttu-id="eba54-131">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="eba54-131">-ClusterName</span></span>
<span data-ttu-id="eba54-132">Der Name des Kusto-Clusters.</span><span class="sxs-lookup"><span data-stu-id="eba54-132">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="eba54-133">-Compression</span><span class="sxs-lookup"><span data-stu-id="eba54-133">-Compression</span></span>
<span data-ttu-id="eba54-134">Der Komprimierungstyp für Ereignishubnachrichten.</span><span class="sxs-lookup"><span data-stu-id="eba54-134">The event hub messages compression type.</span></span>

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

### <span data-ttu-id="eba54-135">-ConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="eba54-135">-ConsumerGroup</span></span>
<span data-ttu-id="eba54-136">Die Ereignis-/iot-Hub-Consumergruppe.</span><span class="sxs-lookup"><span data-stu-id="eba54-136">The event/iot hub consumer group.</span></span>

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

### <span data-ttu-id="eba54-137">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="eba54-137">-DatabaseName</span></span>
<span data-ttu-id="eba54-138">Der Name der Datenbank im Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="eba54-138">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="eba54-139">-DataFormat</span><span class="sxs-lookup"><span data-stu-id="eba54-139">-DataFormat</span></span>
<span data-ttu-id="eba54-140">Das Datenformat der Nachricht.</span><span class="sxs-lookup"><span data-stu-id="eba54-140">The data format of the message.</span></span>
<span data-ttu-id="eba54-141">Optional kann jeder Nachricht das Datenformat hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="eba54-141">Optionally the data format can be added to each message.</span></span>

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

### <span data-ttu-id="eba54-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eba54-142">-DefaultProfile</span></span>
<span data-ttu-id="eba54-143">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="eba54-143">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eba54-144">-EventHubResourceId</span><span class="sxs-lookup"><span data-stu-id="eba54-144">-EventHubResourceId</span></span>
<span data-ttu-id="eba54-145">Die Ressourcen-ID des Ereignishubs, der zum Erstellen einer Datenverbindung/eines Ereignisrasters verwendet werden soll, ist für das Senden von Ereignissen konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="eba54-145">The resource ID of the event hub to be used to create a data connection / event grid is configured to send events.</span></span>

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

### <span data-ttu-id="eba54-146">-EventSystemProperty</span><span class="sxs-lookup"><span data-stu-id="eba54-146">-EventSystemProperty</span></span>
<span data-ttu-id="eba54-147">Systemeigenschaften des Ereignisses/iot-Hubs.</span><span class="sxs-lookup"><span data-stu-id="eba54-147">System properties of the event/iot hub.</span></span>

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

### <span data-ttu-id="eba54-148">-IgnoreFirstRecord</span><span class="sxs-lookup"><span data-stu-id="eba54-148">-IgnoreFirstRecord</span></span>
<span data-ttu-id="eba54-149">Wenn auf "true" festgelegt ist, gibt an, dass bei der Aufnahme der erste Datensatz jeder Datei ignoriert werden soll.</span><span class="sxs-lookup"><span data-stu-id="eba54-149">If set to true, indicates that ingestion should ignore the first record of every file.</span></span>

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

### <span data-ttu-id="eba54-150">-InputObject</span><span class="sxs-lookup"><span data-stu-id="eba54-150">-InputObject</span></span>
<span data-ttu-id="eba54-151">Identitätsparameter Zum Erstellen lesen Sie den Abschnitt NOTIZEN für INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="eba54-151">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="eba54-152">-IotHubResourceId</span><span class="sxs-lookup"><span data-stu-id="eba54-152">-IotHubResourceId</span></span>
<span data-ttu-id="eba54-153">Die Ressourcen-ID des Iot-Hubs, der zum Erstellen einer Datenverbindung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="eba54-153">The resource ID of the Iot hub to be used to create a data connection.</span></span>

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

### <span data-ttu-id="eba54-154">-Kind</span><span class="sxs-lookup"><span data-stu-id="eba54-154">-Kind</span></span>
<span data-ttu-id="eba54-155">Art des Endpunkts für die Datenverbindung</span><span class="sxs-lookup"><span data-stu-id="eba54-155">Kind of the endpoint for the data connection</span></span>

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

### <span data-ttu-id="eba54-156">-Location</span><span class="sxs-lookup"><span data-stu-id="eba54-156">-Location</span></span>
<span data-ttu-id="eba54-157">Ressourcenspeicherort.</span><span class="sxs-lookup"><span data-stu-id="eba54-157">Resource location.</span></span>

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

### <span data-ttu-id="eba54-158">-MappingRuleName</span><span class="sxs-lookup"><span data-stu-id="eba54-158">-MappingRuleName</span></span>
<span data-ttu-id="eba54-159">Die Zuordnungsregel, mit der die Daten aufgenommen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="eba54-159">The mapping rule to be used to ingest the data.</span></span>
<span data-ttu-id="eba54-160">Optional können die Zuordnungsinformationen jeder Nachricht hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="eba54-160">Optionally the mapping information can be added to each message.</span></span>

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

### <span data-ttu-id="eba54-161">-Name</span><span class="sxs-lookup"><span data-stu-id="eba54-161">-Name</span></span>
<span data-ttu-id="eba54-162">Der Name der Datenverbindung.</span><span class="sxs-lookup"><span data-stu-id="eba54-162">The name of the data connection.</span></span>

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

### <span data-ttu-id="eba54-163">-NoWait</span><span class="sxs-lookup"><span data-stu-id="eba54-163">-NoWait</span></span>
<span data-ttu-id="eba54-164">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="eba54-164">Run the command asynchronously</span></span>

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

### <span data-ttu-id="eba54-165">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eba54-165">-ResourceGroupName</span></span>
<span data-ttu-id="eba54-166">Der Name der Ressourcengruppe, die den Kusto-Cluster enthält.</span><span class="sxs-lookup"><span data-stu-id="eba54-166">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="eba54-167">-SharedAccessPolicyName</span><span class="sxs-lookup"><span data-stu-id="eba54-167">-SharedAccessPolicyName</span></span>
<span data-ttu-id="eba54-168">Der Name der Freigabezugriffsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="eba54-168">The name of the share access policy.</span></span>

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

### <span data-ttu-id="eba54-169">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="eba54-169">-StorageAccountResourceId</span></span>
<span data-ttu-id="eba54-170">Die Ressourcen-ID des Speicherkontos, in dem sich die Daten befinden.</span><span class="sxs-lookup"><span data-stu-id="eba54-170">The resource ID of the storage account where the data resides.</span></span>

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

### <span data-ttu-id="eba54-171">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="eba54-171">-SubscriptionId</span></span>
<span data-ttu-id="eba54-172">Ruft Abonnementanmeldeinformationen ab, mit denen Microsoft Azure-Abonnement eindeutig identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="eba54-172">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="eba54-173">Die Abonnement-ID ist Teil des URI für jeden Dienstanruf.</span><span class="sxs-lookup"><span data-stu-id="eba54-173">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="eba54-174">-TableName</span><span class="sxs-lookup"><span data-stu-id="eba54-174">-TableName</span></span>
<span data-ttu-id="eba54-175">Die Tabelle, in der die Daten aufgenommen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="eba54-175">The table where the data should be ingested.</span></span>
<span data-ttu-id="eba54-176">Optional können die Tabelleninformationen jeder Nachricht hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="eba54-176">Optionally the table information can be added to each message.</span></span>

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

### <span data-ttu-id="eba54-177">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="eba54-177">-Confirm</span></span>
<span data-ttu-id="eba54-178">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="eba54-178">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eba54-179">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eba54-179">-WhatIf</span></span>
<span data-ttu-id="eba54-180">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="eba54-180">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eba54-181">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="eba54-181">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eba54-182">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eba54-182">CommonParameters</span></span>
<span data-ttu-id="eba54-183">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eba54-183">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eba54-184">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="eba54-184">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eba54-185">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="eba54-185">INPUTS</span></span>

### <span data-ttu-id="eba54-186">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="eba54-186">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="eba54-187">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="eba54-187">OUTPUTS</span></span>

### <span data-ttu-id="eba54-188">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDataConnection</span><span class="sxs-lookup"><span data-stu-id="eba54-188">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDataConnection</span></span>

## <span data-ttu-id="eba54-189">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="eba54-189">NOTES</span></span>

<span data-ttu-id="eba54-190">ALIASE</span><span class="sxs-lookup"><span data-stu-id="eba54-190">ALIASES</span></span>

<span data-ttu-id="eba54-191">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="eba54-191">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="eba54-192">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="eba54-192">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="eba54-193">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="eba54-193">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="eba54-194">INPUTOBJECT <IKustoIdentity> : Identitätsparameter</span><span class="sxs-lookup"><span data-stu-id="eba54-194">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="eba54-195">`[AttachedDatabaseConfigurationName <String>]`: Der Name der angefügten Datenbankkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="eba54-195">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="eba54-196">`[ClusterName <String>]`: Der Name des Kusto-Clusters.</span><span class="sxs-lookup"><span data-stu-id="eba54-196">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="eba54-197">`[DataConnectionName <String>]`: Der Name der Datenverbindung.</span><span class="sxs-lookup"><span data-stu-id="eba54-197">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="eba54-198">`[DatabaseName <String>]`: Der Name der Datenbank im Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="eba54-198">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="eba54-199">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="eba54-199">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="eba54-200">`[Location <String>]`: Azure-Standort.</span><span class="sxs-lookup"><span data-stu-id="eba54-200">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="eba54-201">`[PrincipalAssignmentName <String>]`: Der Name der Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="eba54-201">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="eba54-202">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die den Kusto-Cluster enthält.</span><span class="sxs-lookup"><span data-stu-id="eba54-202">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="eba54-203">`[SubscriptionId <String>]`: Ruft Abonnementanmeldeinformationen ab, mit denen Microsoft Azure-Abonnement eindeutig identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="eba54-203">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="eba54-204">Die Abonnement-ID ist Teil des URI für jeden Dienstanruf.</span><span class="sxs-lookup"><span data-stu-id="eba54-204">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="eba54-205">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="eba54-205">RELATED LINKS</span></span>

