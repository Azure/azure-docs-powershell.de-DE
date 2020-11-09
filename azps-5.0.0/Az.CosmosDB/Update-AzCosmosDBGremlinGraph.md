---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbgremlingraph
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinGraph.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinGraph.md
ms.openlocfilehash: b69640eb2af37ce0ef48ca3841c3cadcc0c3a57b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94299050"
---
# <span data-ttu-id="10ed9-101">Update-AzCosmosDBGremlinGraph</span><span class="sxs-lookup"><span data-stu-id="10ed9-101">Update-AzCosmosDBGremlinGraph</span></span>

## <span data-ttu-id="10ed9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="10ed9-102">SYNOPSIS</span></span>
<span data-ttu-id="10ed9-103">Aktualisiert das CosmosDB-Gremlin-Diagramm.</span><span class="sxs-lookup"><span data-stu-id="10ed9-103">Updates the CosmosDB Gremlin Graph.</span></span> <span data-ttu-id="10ed9-104">Führt einen clientseitigen Patch-Vorgang durchlesen des vorhandenen Diagramms aus.</span><span class="sxs-lookup"><span data-stu-id="10ed9-104">Performs a client side patch operation by reading the existing Graph.</span></span>

## <span data-ttu-id="10ed9-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="10ed9-105">SYNTAX</span></span>

### <span data-ttu-id="10ed9-106">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="10ed9-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBGremlinGraph -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 [-Name <String>] [-IndexingPolicy <PSIndexingPolicy>] [-PartitionKeyVersion <Int32>]
 [-PartitionKeyKind <String>] [-PartitionKeyPath <String[]>] [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>] [-UniqueKeyPolicy <PSUniqueKeyPolicy>]
 [-ConflictResolutionPolicyMode <String>] [-ConflictResolutionPolicyPath <String>]
 [-ConflictResolutionPolicyProcedure <String>] [-ConflictResolutionPolicy <PSConflictResolutionPolicy>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="10ed9-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="10ed9-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinGraph [-Name <String>] [-IndexingPolicy <PSIndexingPolicy>]
 [-PartitionKeyVersion <Int32>] [-PartitionKeyKind <String>] [-PartitionKeyPath <String[]>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-UniqueKeyPolicy <PSUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSConflictResolutionPolicy>] -ParentObject <PSGremlinDatabaseGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="10ed9-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="10ed9-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinGraph [-Name <String>] [-IndexingPolicy <PSIndexingPolicy>]
 [-PartitionKeyVersion <Int32>] [-PartitionKeyKind <String>] [-PartitionKeyPath <String[]>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-UniqueKeyPolicy <PSUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSConflictResolutionPolicy>] -InputObject <PSGremlinGraphGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="10ed9-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="10ed9-109">DESCRIPTION</span></span>
<span data-ttu-id="10ed9-110">Aktualisiert das CosmosDB-Gremlin-Diagramm.</span><span class="sxs-lookup"><span data-stu-id="10ed9-110">Updates the CosmosDB Gremlin Graph.</span></span> <span data-ttu-id="10ed9-111">Führt einen clientseitigen Patch-Vorgang durchlesen des vorhandenen Diagramms aus.</span><span class="sxs-lookup"><span data-stu-id="10ed9-111">Performs a client side patch operation by reading the existing Graph.</span></span>

## <span data-ttu-id="10ed9-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="10ed9-112">EXAMPLES</span></span>

### <span data-ttu-id="10ed9-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="10ed9-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBGremlinGraph -AccountName myAccountName -DatabaseName myDatabaseName -ResourceGroupName myRgName -Name myContainerName -Throughput updatedThroughputValue

Name     : myContainerName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/gremlinDatabases/myDatabaseName/graphs/myGraphName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetPropertiesResource
```

## <span data-ttu-id="10ed9-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="10ed9-114">PARAMETERS</span></span>

### <span data-ttu-id="10ed9-115">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="10ed9-115">-AccountName</span></span>
<span data-ttu-id="10ed9-116">Name des Cosmos DB-Daten Bankkontos.</span><span class="sxs-lookup"><span data-stu-id="10ed9-116">Name of the Cosmos DB database account.</span></span>

```yaml
Type: String
Parameter Sets: ByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10ed9-117">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="10ed9-117">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="10ed9-118">Maximaler Durchsatz, wenn "AutoScale" aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="10ed9-118">Maximum Throughput value if autoscale is enabled.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10ed9-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="10ed9-119">-Confirm</span></span>
<span data-ttu-id="10ed9-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="10ed9-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10ed9-121">-ConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="10ed9-121">-ConflictResolutionPolicy</span></span>
<span data-ttu-id="10ed9-122">ConflictResolutionPolicy-Objekt vom Typ PSConflictResolutionPolicy, wenn diese Einstellung als ConflictResolutionPolicy des Containers angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="10ed9-122">ConflictResolutionPolicy Object of type PSConflictResolutionPolicy, when provided this is set as the ConflictResolutionPolicy of the container.</span></span>

```yaml
Type: PSConflictResolutionPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="10ed9-123">-ConflictResolutionPolicyMode</span><span class="sxs-lookup"><span data-stu-id="10ed9-123">-ConflictResolutionPolicyMode</span></span>
<span data-ttu-id="10ed9-124">Kann die Werte haben: LastWriterWins, Benutzerdefiniert, manuell.</span><span class="sxs-lookup"><span data-stu-id="10ed9-124">Can have the values: LastWriterWins, Custom, Manual.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10ed9-125">-ConflictResolutionPolicyPath</span><span class="sxs-lookup"><span data-stu-id="10ed9-125">-ConflictResolutionPolicyPath</span></span>
<span data-ttu-id="10ed9-126">, Die bereitgestellt werden soll, wenn der Typ LastWriterWins ist.</span><span class="sxs-lookup"><span data-stu-id="10ed9-126">To be provided when the type is LastWriterWins.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10ed9-127">-ConflictResolutionPolicyProcedure</span><span class="sxs-lookup"><span data-stu-id="10ed9-127">-ConflictResolutionPolicyProcedure</span></span>
<span data-ttu-id="10ed9-128">, Die bereitgestellt werden soll, wenn der Typ Benutzerdefiniert ist.</span><span class="sxs-lookup"><span data-stu-id="10ed9-128">To be provided when the type is custom.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10ed9-129">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="10ed9-129">-DatabaseName</span></span>
<span data-ttu-id="10ed9-130">Datenbankname</span><span class="sxs-lookup"><span data-stu-id="10ed9-130">Database name.</span></span>

```yaml
Type: String
Parameter Sets: ByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10ed9-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10ed9-131">-DefaultProfile</span></span>
<span data-ttu-id="10ed9-132">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="10ed9-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10ed9-133">-IndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="10ed9-133">-IndexingPolicy</span></span>
<span data-ttu-id="10ed9-134">Indizierungs Richtlinienobjekt vom Typ Microsoft. Azure. Commands. CosmosDB. PSIndexingPolicy.</span><span class="sxs-lookup"><span data-stu-id="10ed9-134">Indexing Policy Object of type Microsoft.Azure.Commands.CosmosDB.PSIndexingPolicy.</span></span>

```yaml
Type: PSIndexingPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="10ed9-135">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="10ed9-135">-InputObject</span></span>
<span data-ttu-id="10ed9-136">Gremlin-Diagrammobjekt</span><span class="sxs-lookup"><span data-stu-id="10ed9-136">Gremlin Graph object.</span></span>

```yaml
Type: PSGremlinGraphGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="10ed9-137">-Name</span><span class="sxs-lookup"><span data-stu-id="10ed9-137">-Name</span></span>
<span data-ttu-id="10ed9-138">Gremlin-Diagramm Name</span><span class="sxs-lookup"><span data-stu-id="10ed9-138">Gremlin Graph Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10ed9-139">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="10ed9-139">-ParentObject</span></span>
<span data-ttu-id="10ed9-140">Gremlin-Datenbankobjekt.</span><span class="sxs-lookup"><span data-stu-id="10ed9-140">Gremlin Database object.</span></span>

```yaml
Type: PSGremlinDatabaseGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="10ed9-141">-PartitionKeyKind</span><span class="sxs-lookup"><span data-stu-id="10ed9-141">-PartitionKeyKind</span></span>
<span data-ttu-id="10ed9-142">Die Art des für die Partitionierung verwendeten Algorithmus.</span><span class="sxs-lookup"><span data-stu-id="10ed9-142">The kind of algorithm used for partitioning.</span></span>
<span data-ttu-id="10ed9-143">Mögliche Werte sind: "Hash"; "Bereich"</span><span class="sxs-lookup"><span data-stu-id="10ed9-143">Possible values include: 'Hash', 'Range'</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10ed9-144">-PartitionKeyPath</span><span class="sxs-lookup"><span data-stu-id="10ed9-144">-PartitionKeyPath</span></span>
<span data-ttu-id="10ed9-145">Partitionsschlüssel Pfad, beispielsweise "/Address/ZipCode".</span><span class="sxs-lookup"><span data-stu-id="10ed9-145">Partition Key Path, e.g., '/address/zipcode'.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10ed9-146">-PartitionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="10ed9-146">-PartitionKeyVersion</span></span>
<span data-ttu-id="10ed9-147">Die Version der Partitionsschlüssel Definition</span><span class="sxs-lookup"><span data-stu-id="10ed9-147">The version of the partition key definition</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10ed9-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10ed9-148">-ResourceGroupName</span></span>
<span data-ttu-id="10ed9-149">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="10ed9-149">Name of resource group.</span></span>

```yaml
Type: String
Parameter Sets: ByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10ed9-150">-Durchsatz</span><span class="sxs-lookup"><span data-stu-id="10ed9-150">-Throughput</span></span>
<span data-ttu-id="10ed9-151">Der Durchsatz von Gremlin Graph (ru/s).</span><span class="sxs-lookup"><span data-stu-id="10ed9-151">The throughput of Gremlin Graph (RU/s).</span></span>
<span data-ttu-id="10ed9-152">Der Standardwert ist 400.</span><span class="sxs-lookup"><span data-stu-id="10ed9-152">Default value is 400.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10ed9-153">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="10ed9-153">-TtlInSeconds</span></span>
<span data-ttu-id="10ed9-154">Standard-TTL in Sekunden.</span><span class="sxs-lookup"><span data-stu-id="10ed9-154">Default Ttl in seconds.</span></span>
<span data-ttu-id="10ed9-155">Wenn der Wert fehlt oder auf-1 gesetzt ist, werden die Elemente nicht ablaufen.</span><span class="sxs-lookup"><span data-stu-id="10ed9-155">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="10ed9-156">Wenn der Wert auf n gesetzt ist, werden die Elemente nach dem Zeitpunkt der letzten Änderung n Sekunden ablaufen.</span><span class="sxs-lookup"><span data-stu-id="10ed9-156">If the value is set to n, items will expire n seconds after last modified time.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10ed9-157">-UniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="10ed9-157">-UniqueKeyPolicy</span></span>
<span data-ttu-id="10ed9-158">UniqueKeyPolicy-Objekt vom Typ Microsoft. Azure. Commands. CosmosDB. PSUniqueKeyPolicy.</span><span class="sxs-lookup"><span data-stu-id="10ed9-158">UniqueKeyPolicy Object of type Microsoft.Azure.Commands.CosmosDB.PSUniqueKeyPolicy.</span></span>

```yaml
Type: PSUniqueKeyPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="10ed9-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="10ed9-159">-WhatIf</span></span>
<span data-ttu-id="10ed9-160">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="10ed9-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="10ed9-161">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="10ed9-161">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10ed9-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10ed9-162">CommonParameters</span></span>
<span data-ttu-id="10ed9-163">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10ed9-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10ed9-164">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="10ed9-164">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10ed9-165">Eingaben</span><span class="sxs-lookup"><span data-stu-id="10ed9-165">INPUTS</span></span>

### <span data-ttu-id="10ed9-166">Microsoft. Azure. Commands. CosmosDB. Models. PSIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="10ed9-166">Microsoft.Azure.Commands.CosmosDB.Models.PSIndexingPolicy</span></span>

### <span data-ttu-id="10ed9-167">Microsoft. Azure. Commands. CosmosDB. Models. PSUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="10ed9-167">Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKeyPolicy</span></span>

### <span data-ttu-id="10ed9-168">Microsoft. Azure. Commands. CosmosDB. Models. PSConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="10ed9-168">Microsoft.Azure.Commands.CosmosDB.Models.PSConflictResolutionPolicy</span></span>

### <span data-ttu-id="10ed9-169">Microsoft. Azure. Commands. CosmosDB. Models. PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="10ed9-169">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

### <span data-ttu-id="10ed9-170">Microsoft. Azure. Commands. CosmosDB. Models. PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="10ed9-170">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

## <span data-ttu-id="10ed9-171">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="10ed9-171">OUTPUTS</span></span>

### <span data-ttu-id="10ed9-172">Microsoft. Azure. Commands. CosmosDB. Models. PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="10ed9-172">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

### <span data-ttu-id="10ed9-173">Microsoft. Azure. Commands. CosmosDB. Exceptions. ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="10ed9-173">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="10ed9-174">Notizen</span><span class="sxs-lookup"><span data-stu-id="10ed9-174">NOTES</span></span>

## <span data-ttu-id="10ed9-175">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="10ed9-175">RELATED LINKS</span></span>
