---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbsqlcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlContainer.md
ms.openlocfilehash: 85f220c7745f28a2786e9a26edc86baa129c3c3c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94175280"
---
# <span data-ttu-id="a1b88-101">Update-AzCosmosDBSqlContainer</span><span class="sxs-lookup"><span data-stu-id="a1b88-101">Update-AzCosmosDBSqlContainer</span></span>

## <span data-ttu-id="a1b88-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a1b88-102">SYNOPSIS</span></span>
<span data-ttu-id="a1b88-103">Aktualisiert den CosmosDB-SQL-Container.</span><span class="sxs-lookup"><span data-stu-id="a1b88-103">Updates the CosmosDB Sql Container.</span></span> <span data-ttu-id="a1b88-104">Führt einen clientseitigen Patch-Vorgang durchlesen des vorhandenen Containers durch.</span><span class="sxs-lookup"><span data-stu-id="a1b88-104">Performs a client side patch operation by reading the existing Container.</span></span>

## <span data-ttu-id="a1b88-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a1b88-105">SYNTAX</span></span>

### <span data-ttu-id="a1b88-106">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="a1b88-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBSqlContainer -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 [-Name <String>] [-IndexingPolicy <PSSqlIndexingPolicy>] [-PartitionKeyVersion <Int32>]
 [-PartitionKeyKind <String>] [-PartitionKeyPath <String[]>] [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>] [-UniqueKeyPolicy <PSSqlUniqueKeyPolicy>]
 [-ConflictResolutionPolicyMode <String>] [-ConflictResolutionPolicyPath <String>]
 [-ConflictResolutionPolicyProcedure <String>] [-ConflictResolutionPolicy <PSSqlConflictResolutionPolicy>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1b88-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a1b88-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlContainer [-Name <String>] [-IndexingPolicy <PSSqlIndexingPolicy>]
 [-PartitionKeyVersion <Int32>] [-PartitionKeyKind <String>] [-PartitionKeyPath <String[]>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-UniqueKeyPolicy <PSSqlUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSSqlConflictResolutionPolicy>] -ParentObject <PSSqlDatabaseGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1b88-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a1b88-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlContainer [-Name <String>] [-IndexingPolicy <PSSqlIndexingPolicy>]
 [-PartitionKeyVersion <Int32>] [-PartitionKeyKind <String>] [-PartitionKeyPath <String[]>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-UniqueKeyPolicy <PSSqlUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSSqlConflictResolutionPolicy>] -InputObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a1b88-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a1b88-109">DESCRIPTION</span></span>
<span data-ttu-id="a1b88-110">Aktualisiert den CosmosDB-SQL-Container.</span><span class="sxs-lookup"><span data-stu-id="a1b88-110">Updates the CosmosDB Sql Container.</span></span> <span data-ttu-id="a1b88-111">Führt einen clientseitigen Patch-Vorgang durchlesen des vorhandenen Containers durch.</span><span class="sxs-lookup"><span data-stu-id="a1b88-111">Performs a client side patch operation by reading the existing Container.</span></span>

## <span data-ttu-id="a1b88-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a1b88-112">EXAMPLES</span></span>

### <span data-ttu-id="a1b88-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a1b88-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBMongoDBDatabase -AccountName myAccountName -Name myDatabaseName -ResourceGroupName myResourcegroupName -Throughput 800

Name     : myDatabaseName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/mongodbDatabases/myDatabaseName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetPropertiesResource
```

## <span data-ttu-id="a1b88-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="a1b88-114">PARAMETERS</span></span>

### <span data-ttu-id="a1b88-115">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="a1b88-115">-AccountName</span></span>
<span data-ttu-id="a1b88-116">Name des Cosmos DB-Daten Bankkontos.</span><span class="sxs-lookup"><span data-stu-id="a1b88-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="a1b88-117">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="a1b88-117">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="a1b88-118">Maximaler Durchsatz, wenn "AutoScale" aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="a1b88-118">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="a1b88-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a1b88-119">-Confirm</span></span>
<span data-ttu-id="a1b88-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a1b88-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a1b88-121">-ConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="a1b88-121">-ConflictResolutionPolicy</span></span>
<span data-ttu-id="a1b88-122">ConflictResolutionPolicy-Objekt vom Typ PSSqlConflictResolutionPolicy, wenn diese Einstellung als ConflictResolutionPolicy des Containers angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="a1b88-122">ConflictResolutionPolicy Object of type PSSqlConflictResolutionPolicy, when provided this is set as the ConflictResolutionPolicy of the container.</span></span>

```yaml
Type: PSSqlConflictResolutionPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a1b88-123">-ConflictResolutionPolicyMode</span><span class="sxs-lookup"><span data-stu-id="a1b88-123">-ConflictResolutionPolicyMode</span></span>
<span data-ttu-id="a1b88-124">Kann die Werte haben: LastWriterWins, Benutzerdefiniert, manuell.</span><span class="sxs-lookup"><span data-stu-id="a1b88-124">Can have the values: LastWriterWins, Custom, Manual.</span></span>
<span data-ttu-id="a1b88-125">Wenn Sie zusammen mit dem ConflictResolutionPolicy-Parameter bereitgestellt werden, wird Sie ignoriert.</span><span class="sxs-lookup"><span data-stu-id="a1b88-125">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

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

### <span data-ttu-id="a1b88-126">-ConflictResolutionPolicyPath</span><span class="sxs-lookup"><span data-stu-id="a1b88-126">-ConflictResolutionPolicyPath</span></span>
<span data-ttu-id="a1b88-127">, Die bereitgestellt werden soll, wenn der Typ LastWriterWins ist.</span><span class="sxs-lookup"><span data-stu-id="a1b88-127">To be provided when the type is LastWriterWins.</span></span>
<span data-ttu-id="a1b88-128">Wenn Sie zusammen mit dem ConflictResolutionPolicy-Parameter bereitgestellt werden, wird Sie ignoriert.</span><span class="sxs-lookup"><span data-stu-id="a1b88-128">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

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

### <span data-ttu-id="a1b88-129">-ConflictResolutionPolicyProcedure</span><span class="sxs-lookup"><span data-stu-id="a1b88-129">-ConflictResolutionPolicyProcedure</span></span>
<span data-ttu-id="a1b88-130">, Die bereitgestellt werden soll, wenn der Typ Benutzerdefiniert ist.</span><span class="sxs-lookup"><span data-stu-id="a1b88-130">To be provided when the type is custom.</span></span>
<span data-ttu-id="a1b88-131">Wenn Sie zusammen mit dem ConflictResolutionPolicy-Parameter bereitgestellt werden, wird Sie ignoriert.</span><span class="sxs-lookup"><span data-stu-id="a1b88-131">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

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

### <span data-ttu-id="a1b88-132">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="a1b88-132">-DatabaseName</span></span>
<span data-ttu-id="a1b88-133">Datenbankname</span><span class="sxs-lookup"><span data-stu-id="a1b88-133">Database name.</span></span>

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

### <span data-ttu-id="a1b88-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1b88-134">-DefaultProfile</span></span>
<span data-ttu-id="a1b88-135">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a1b88-135">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a1b88-136">-IndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="a1b88-136">-IndexingPolicy</span></span>
<span data-ttu-id="a1b88-137">Indizierungs Richtlinienobjekt vom Typ Microsoft. Azure. Commands. CosmosDB. PSSqlIndexingPolicy.</span><span class="sxs-lookup"><span data-stu-id="a1b88-137">Indexing Policy Object of type Microsoft.Azure.Commands.CosmosDB.PSSqlIndexingPolicy.</span></span>

```yaml
Type: PSSqlIndexingPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a1b88-138">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="a1b88-138">-InputObject</span></span>
<span data-ttu-id="a1b88-139">SQL-Container Objekt.</span><span class="sxs-lookup"><span data-stu-id="a1b88-139">Sql Container object.</span></span>

```yaml
Type: PSSqlContainerGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a1b88-140">-Name</span><span class="sxs-lookup"><span data-stu-id="a1b88-140">-Name</span></span>
<span data-ttu-id="a1b88-141">Container Name.</span><span class="sxs-lookup"><span data-stu-id="a1b88-141">Container name.</span></span>

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

### <span data-ttu-id="a1b88-142">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="a1b88-142">-ParentObject</span></span>
<span data-ttu-id="a1b88-143">SQL-Datenbankobjekt.</span><span class="sxs-lookup"><span data-stu-id="a1b88-143">Sql Database object.</span></span>

```yaml
Type: PSSqlDatabaseGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a1b88-144">-PartitionKeyKind</span><span class="sxs-lookup"><span data-stu-id="a1b88-144">-PartitionKeyKind</span></span>
<span data-ttu-id="a1b88-145">Die Art des für die Partitionierung verwendeten Algorithmus.</span><span class="sxs-lookup"><span data-stu-id="a1b88-145">The kind of algorithm used for partitioning.</span></span>
<span data-ttu-id="a1b88-146">Mögliche Werte sind: "Hash"; "Bereich"</span><span class="sxs-lookup"><span data-stu-id="a1b88-146">Possible values include: 'Hash', 'Range'</span></span>

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

### <span data-ttu-id="a1b88-147">-PartitionKeyPath</span><span class="sxs-lookup"><span data-stu-id="a1b88-147">-PartitionKeyPath</span></span>
<span data-ttu-id="a1b88-148">Partitionsschlüssel Pfad, beispielsweise "/Address/ZipCode".</span><span class="sxs-lookup"><span data-stu-id="a1b88-148">Partition Key Path, e.g., '/address/zipcode'.</span></span>

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

### <span data-ttu-id="a1b88-149">-PartitionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="a1b88-149">-PartitionKeyVersion</span></span>
<span data-ttu-id="a1b88-150">Die Version der Partitionsschlüssel Definition</span><span class="sxs-lookup"><span data-stu-id="a1b88-150">The version of the partition key definition</span></span>

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

### <span data-ttu-id="a1b88-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1b88-151">-ResourceGroupName</span></span>
<span data-ttu-id="a1b88-152">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="a1b88-152">Name of resource group.</span></span>

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

### <span data-ttu-id="a1b88-153">-Durchsatz</span><span class="sxs-lookup"><span data-stu-id="a1b88-153">-Throughput</span></span>
<span data-ttu-id="a1b88-154">Der Durchsatz des SQL-Containers (ru/s).</span><span class="sxs-lookup"><span data-stu-id="a1b88-154">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="a1b88-155">Der Standardwert ist 400.</span><span class="sxs-lookup"><span data-stu-id="a1b88-155">Default value is 400.</span></span>

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

### <span data-ttu-id="a1b88-156">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="a1b88-156">-TtlInSeconds</span></span>
<span data-ttu-id="a1b88-157">Standard-TTL in Sekunden.</span><span class="sxs-lookup"><span data-stu-id="a1b88-157">Default Ttl in seconds.</span></span>
<span data-ttu-id="a1b88-158">Wenn der Wert fehlt oder auf-1 gesetzt ist, werden die Elemente nicht ablaufen.</span><span class="sxs-lookup"><span data-stu-id="a1b88-158">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="a1b88-159">Wenn der Wert auf n gesetzt ist, werden die Elemente nach dem Zeitpunkt der letzten Änderung n Sekunden ablaufen.</span><span class="sxs-lookup"><span data-stu-id="a1b88-159">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="a1b88-160">-UniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="a1b88-160">-UniqueKeyPolicy</span></span>
<span data-ttu-id="a1b88-161">UniqueKeyPolicy-Objekt vom Typ Microsoft. Azure. Commands. CosmosDB. PSSqlUniqueKeyPolicy.</span><span class="sxs-lookup"><span data-stu-id="a1b88-161">UniqueKeyPolicy Object of type Microsoft.Azure.Commands.CosmosDB.PSSqlUniqueKeyPolicy.</span></span>

```yaml
Type: PSSqlUniqueKeyPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a1b88-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1b88-162">-WhatIf</span></span>
<span data-ttu-id="a1b88-163">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a1b88-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a1b88-164">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a1b88-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a1b88-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1b88-165">CommonParameters</span></span>
<span data-ttu-id="a1b88-166">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1b88-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1b88-167">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a1b88-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1b88-168">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a1b88-168">INPUTS</span></span>

### <span data-ttu-id="a1b88-169">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="a1b88-169">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlIndexingPolicy</span></span>

### <span data-ttu-id="a1b88-170">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="a1b88-170">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKeyPolicy</span></span>

### <span data-ttu-id="a1b88-171">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="a1b88-171">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlConflictResolutionPolicy</span></span>

### <span data-ttu-id="a1b88-172">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="a1b88-172">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="a1b88-173">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="a1b88-173">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

## <span data-ttu-id="a1b88-174">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a1b88-174">OUTPUTS</span></span>

### <span data-ttu-id="a1b88-175">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="a1b88-175">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="a1b88-176">Microsoft. Azure. Commands. CosmosDB. Exceptions. ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="a1b88-176">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="a1b88-177">Notizen</span><span class="sxs-lookup"><span data-stu-id="a1b88-177">NOTES</span></span>

## <span data-ttu-id="a1b88-178">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a1b88-178">RELATED LINKS</span></span>
