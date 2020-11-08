---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqlcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlContainer.md
ms.openlocfilehash: afdd1296b01a6798d9253b7b21d15ba66f924c34
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94008579"
---
# <span data-ttu-id="d39c3-101">New-AzCosmosDBSqlContainer</span><span class="sxs-lookup"><span data-stu-id="d39c3-101">New-AzCosmosDBSqlContainer</span></span>

## <span data-ttu-id="d39c3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d39c3-102">SYNOPSIS</span></span>
<span data-ttu-id="d39c3-103">Erstellt einen neuen CosmosDB-SQL-Container.</span><span class="sxs-lookup"><span data-stu-id="d39c3-103">Creates a new CosmosDB Sql Container.</span></span>

## <span data-ttu-id="d39c3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d39c3-104">SYNTAX</span></span>

### <span data-ttu-id="d39c3-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="d39c3-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBSqlContainer -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-IndexingPolicy <PSSqlIndexingPolicy>] [-PartitionKeyVersion <Int32>]
 -PartitionKeyKind <String> -PartitionKeyPath <String[]> [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>] [-UniqueKeyPolicy <PSSqlUniqueKeyPolicy>]
 [-ConflictResolutionPolicyMode <String>] [-ConflictResolutionPolicyPath <String>]
 [-ConflictResolutionPolicyProcedure <String>] [-ConflictResolutionPolicy <PSSqlConflictResolutionPolicy>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d39c3-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d39c3-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBSqlContainer -Name <String> [-IndexingPolicy <PSSqlIndexingPolicy>]
 [-PartitionKeyVersion <Int32>] -PartitionKeyKind <String> -PartitionKeyPath <String[]> [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>] [-UniqueKeyPolicy <PSSqlUniqueKeyPolicy>]
 [-ConflictResolutionPolicyMode <String>] [-ConflictResolutionPolicyPath <String>]
 [-ConflictResolutionPolicyProcedure <String>] [-ConflictResolutionPolicy <PSSqlConflictResolutionPolicy>]
 -ParentObject <PSSqlDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d39c3-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d39c3-107">DESCRIPTION</span></span>
<span data-ttu-id="d39c3-108">Erstellt einen neuen CosmosDB-SQL-Container.</span><span class="sxs-lookup"><span data-stu-id="d39c3-108">Creates a new CosmosDB Sql Container.</span></span>

## <span data-ttu-id="d39c3-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d39c3-109">EXAMPLES</span></span>

### <span data-ttu-id="d39c3-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d39c3-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlContainer -AccountName myAccountName -DatabaseName myDatabaseName -ResourceGroupName myRgName -Name myContainerName -PartitionKeyPath /a/b/c -PartitionKeyKind Hash

Name     : myContainerName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/sqlDatabases/myDatabaseName/contain
           ers/myContainerName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetPropertiesResource
```

## <span data-ttu-id="d39c3-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="d39c3-111">PARAMETERS</span></span>

### <span data-ttu-id="d39c3-112">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="d39c3-112">-AccountName</span></span>
<span data-ttu-id="d39c3-113">Name des Cosmos DB-Daten Bankkontos.</span><span class="sxs-lookup"><span data-stu-id="d39c3-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="d39c3-114">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="d39c3-114">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="d39c3-115">Maximaler Durchsatz, wenn "AutoScale" aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="d39c3-115">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="d39c3-116">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d39c3-116">-Confirm</span></span>
<span data-ttu-id="d39c3-117">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d39c3-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d39c3-118">-ConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="d39c3-118">-ConflictResolutionPolicy</span></span>
<span data-ttu-id="d39c3-119">ConflictResolutionPolicy-Objekt vom Typ PSSqlConflictResolutionPolicy, wenn diese Einstellung als ConflictResolutionPolicy des Containers angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="d39c3-119">ConflictResolutionPolicy Object of type PSSqlConflictResolutionPolicy, when provided this is set as the ConflictResolutionPolicy of the container.</span></span>

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

### <span data-ttu-id="d39c3-120">-ConflictResolutionPolicyMode</span><span class="sxs-lookup"><span data-stu-id="d39c3-120">-ConflictResolutionPolicyMode</span></span>
<span data-ttu-id="d39c3-121">Kann die Werte haben: LastWriterWins, Benutzerdefiniert, manuell.</span><span class="sxs-lookup"><span data-stu-id="d39c3-121">Can have the values: LastWriterWins, Custom, Manual.</span></span>
<span data-ttu-id="d39c3-122">Wenn Sie zusammen mit dem ConflictResolutionPolicy-Parameter bereitgestellt werden, wird Sie ignoriert.</span><span class="sxs-lookup"><span data-stu-id="d39c3-122">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

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

### <span data-ttu-id="d39c3-123">-ConflictResolutionPolicyPath</span><span class="sxs-lookup"><span data-stu-id="d39c3-123">-ConflictResolutionPolicyPath</span></span>
<span data-ttu-id="d39c3-124">, Die bereitgestellt werden soll, wenn der Typ LastWriterWins ist.</span><span class="sxs-lookup"><span data-stu-id="d39c3-124">To be provided when the type is LastWriterWins.</span></span>
<span data-ttu-id="d39c3-125">Wenn Sie zusammen mit dem ConflictResolutionPolicy-Parameter bereitgestellt werden, wird Sie ignoriert.</span><span class="sxs-lookup"><span data-stu-id="d39c3-125">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

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

### <span data-ttu-id="d39c3-126">-ConflictResolutionPolicyProcedure</span><span class="sxs-lookup"><span data-stu-id="d39c3-126">-ConflictResolutionPolicyProcedure</span></span>
<span data-ttu-id="d39c3-127">, Die bereitgestellt werden soll, wenn der Typ Benutzerdefiniert ist.</span><span class="sxs-lookup"><span data-stu-id="d39c3-127">To be provided when the type is custom.</span></span>
<span data-ttu-id="d39c3-128">Wenn Sie zusammen mit dem ConflictResolutionPolicy-Parameter bereitgestellt werden, wird Sie ignoriert.</span><span class="sxs-lookup"><span data-stu-id="d39c3-128">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

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

### <span data-ttu-id="d39c3-129">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d39c3-129">-DatabaseName</span></span>
<span data-ttu-id="d39c3-130">Datenbankname</span><span class="sxs-lookup"><span data-stu-id="d39c3-130">Database name.</span></span>

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

### <span data-ttu-id="d39c3-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d39c3-131">-DefaultProfile</span></span>
<span data-ttu-id="d39c3-132">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d39c3-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d39c3-133">-IndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="d39c3-133">-IndexingPolicy</span></span>
<span data-ttu-id="d39c3-134">Indizierungs Richtlinienobjekt vom Typ Microsoft. Azure. Commands. CosmosDB. PSSqlIndexingPolicy.</span><span class="sxs-lookup"><span data-stu-id="d39c3-134">Indexing Policy Object of type Microsoft.Azure.Commands.CosmosDB.PSSqlIndexingPolicy.</span></span>

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

### <span data-ttu-id="d39c3-135">-Name</span><span class="sxs-lookup"><span data-stu-id="d39c3-135">-Name</span></span>
<span data-ttu-id="d39c3-136">Container Name.</span><span class="sxs-lookup"><span data-stu-id="d39c3-136">Container name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d39c3-137">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="d39c3-137">-ParentObject</span></span>
<span data-ttu-id="d39c3-138">SQL-Datenbankobjekt.</span><span class="sxs-lookup"><span data-stu-id="d39c3-138">Sql Database object.</span></span>

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

### <span data-ttu-id="d39c3-139">-PartitionKeyKind</span><span class="sxs-lookup"><span data-stu-id="d39c3-139">-PartitionKeyKind</span></span>
<span data-ttu-id="d39c3-140">Die Art des für die Partitionierung verwendeten Algorithmus.</span><span class="sxs-lookup"><span data-stu-id="d39c3-140">The kind of algorithm used for partitioning.</span></span>
<span data-ttu-id="d39c3-141">Mögliche Werte sind: "Hash"; "Bereich"</span><span class="sxs-lookup"><span data-stu-id="d39c3-141">Possible values include: 'Hash', 'Range'</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d39c3-142">-PartitionKeyPath</span><span class="sxs-lookup"><span data-stu-id="d39c3-142">-PartitionKeyPath</span></span>
<span data-ttu-id="d39c3-143">Partitionsschlüssel Pfad, beispielsweise "/Address/ZipCode".</span><span class="sxs-lookup"><span data-stu-id="d39c3-143">Partition Key Path, e.g., '/address/zipcode'.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d39c3-144">-PartitionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="d39c3-144">-PartitionKeyVersion</span></span>
<span data-ttu-id="d39c3-145">Die Version der Partitionsschlüssel Definition</span><span class="sxs-lookup"><span data-stu-id="d39c3-145">The version of the partition key definition</span></span>

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

### <span data-ttu-id="d39c3-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d39c3-146">-ResourceGroupName</span></span>
<span data-ttu-id="d39c3-147">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="d39c3-147">Name of resource group.</span></span>

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

### <span data-ttu-id="d39c3-148">-Durchsatz</span><span class="sxs-lookup"><span data-stu-id="d39c3-148">-Throughput</span></span>
<span data-ttu-id="d39c3-149">Der Durchsatz des SQL-Containers (ru/s).</span><span class="sxs-lookup"><span data-stu-id="d39c3-149">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="d39c3-150">Der Standardwert ist 400.</span><span class="sxs-lookup"><span data-stu-id="d39c3-150">Default value is 400.</span></span>

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

### <span data-ttu-id="d39c3-151">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="d39c3-151">-TtlInSeconds</span></span>
<span data-ttu-id="d39c3-152">Standard-TTL in Sekunden.</span><span class="sxs-lookup"><span data-stu-id="d39c3-152">Default Ttl in seconds.</span></span>
<span data-ttu-id="d39c3-153">Wenn der Wert fehlt oder auf-1 gesetzt ist, werden die Elemente nicht ablaufen.</span><span class="sxs-lookup"><span data-stu-id="d39c3-153">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="d39c3-154">Wenn der Wert auf n gesetzt ist, werden die Elemente nach dem Zeitpunkt der letzten Änderung n Sekunden ablaufen.</span><span class="sxs-lookup"><span data-stu-id="d39c3-154">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="d39c3-155">-UniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="d39c3-155">-UniqueKeyPolicy</span></span>
<span data-ttu-id="d39c3-156">UniqueKeyPolicy-Objekt vom Typ Microsoft. Azure. Commands. CosmosDB. PSSqlUniqueKeyPolicy.</span><span class="sxs-lookup"><span data-stu-id="d39c3-156">UniqueKeyPolicy Object of type Microsoft.Azure.Commands.CosmosDB.PSSqlUniqueKeyPolicy.</span></span>

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

### <span data-ttu-id="d39c3-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d39c3-157">-WhatIf</span></span>
<span data-ttu-id="d39c3-158">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d39c3-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d39c3-159">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d39c3-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d39c3-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d39c3-160">CommonParameters</span></span>
<span data-ttu-id="d39c3-161">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d39c3-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d39c3-162">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d39c3-162">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d39c3-163">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d39c3-163">INPUTS</span></span>

### <span data-ttu-id="d39c3-164">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="d39c3-164">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlIndexingPolicy</span></span>

### <span data-ttu-id="d39c3-165">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="d39c3-165">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKeyPolicy</span></span>

### <span data-ttu-id="d39c3-166">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="d39c3-166">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlConflictResolutionPolicy</span></span>

### <span data-ttu-id="d39c3-167">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="d39c3-167">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

## <span data-ttu-id="d39c3-168">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d39c3-168">OUTPUTS</span></span>

### <span data-ttu-id="d39c3-169">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="d39c3-169">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="d39c3-170">Microsoft. Azure. Commands. CosmosDB. Exceptions. ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="d39c3-170">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="d39c3-171">Notizen</span><span class="sxs-lookup"><span data-stu-id="d39c3-171">NOTES</span></span>

## <span data-ttu-id="d39c3-172">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d39c3-172">RELATED LINKS</span></span>
