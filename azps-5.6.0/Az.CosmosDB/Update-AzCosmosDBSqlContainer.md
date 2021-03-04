---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/update-azcosmosdbsqlcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlContainer.md
ms.openlocfilehash: a36222b3a6cacf567fd0b5e7541c2dc53a44fa22
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101931248"
---
# <span data-ttu-id="ae3ca-101">Update-AzCosmosDBSqlContainer</span><span class="sxs-lookup"><span data-stu-id="ae3ca-101">Update-AzCosmosDBSqlContainer</span></span>

## <span data-ttu-id="ae3ca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ae3ca-102">SYNOPSIS</span></span>
<span data-ttu-id="ae3ca-103">Aktualisiert den CosmosDB Sql Container.</span><span class="sxs-lookup"><span data-stu-id="ae3ca-103">Updates the CosmosDB Sql Container.</span></span> <span data-ttu-id="ae3ca-104">Führt einen clientseitigen Patchvorgang durch Lesen des vorhandenen Containers aus.</span><span class="sxs-lookup"><span data-stu-id="ae3ca-104">Performs a client side patch operation by reading the existing Container.</span></span>

## <span data-ttu-id="ae3ca-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ae3ca-105">SYNTAX</span></span>

### <span data-ttu-id="ae3ca-106">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="ae3ca-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBSqlContainer -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 [-Name <String>] [-IndexingPolicy <PSSqlIndexingPolicy>] [-PartitionKeyVersion <Int32>]
 [-PartitionKeyKind <String>] [-PartitionKeyPath <String[]>] [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>] [-UniqueKeyPolicy <PSSqlUniqueKeyPolicy>]
 [-ConflictResolutionPolicyMode <String>] [-ConflictResolutionPolicyPath <String>]
 [-ConflictResolutionPolicyProcedure <String>] [-ConflictResolutionPolicy <PSSqlConflictResolutionPolicy>]
 [-AnalyticalStorageTtl <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ae3ca-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ae3ca-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlContainer [-Name <String>] [-IndexingPolicy <PSSqlIndexingPolicy>]
 [-PartitionKeyVersion <Int32>] [-PartitionKeyKind <String>] [-PartitionKeyPath <String[]>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-UniqueKeyPolicy <PSSqlUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSSqlConflictResolutionPolicy>] -ParentObject <PSSqlDatabaseGetResults>
 [-AnalyticalStorageTtl <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ae3ca-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ae3ca-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlContainer [-Name <String>] [-IndexingPolicy <PSSqlIndexingPolicy>]
 [-PartitionKeyVersion <Int32>] [-PartitionKeyKind <String>] [-PartitionKeyPath <String[]>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-UniqueKeyPolicy <PSSqlUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSSqlConflictResolutionPolicy>] [-AnalyticalStorageTtl <Int32>]
 -InputObject <PSSqlContainerGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ae3ca-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ae3ca-109">DESCRIPTION</span></span>
<span data-ttu-id="ae3ca-110">Aktualisiert den CosmosDB Sql Container.</span><span class="sxs-lookup"><span data-stu-id="ae3ca-110">Updates the CosmosDB Sql Container.</span></span> <span data-ttu-id="ae3ca-111">Führt einen clientseitigen Patchvorgang durch Lesen des vorhandenen Containers aus.</span><span class="sxs-lookup"><span data-stu-id="ae3ca-111">Performs a client side patch operation by reading the existing Container.</span></span>

## <span data-ttu-id="ae3ca-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ae3ca-112">EXAMPLES</span></span>

### <span data-ttu-id="ae3ca-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ae3ca-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBMongoDBDatabase -AccountName myAccountName -Name myDatabaseName -ResourceGroupName myResourcegroupName -Throughput 800

Name     : myDatabaseName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/mongodbDatabases/myDatabaseName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetPropertiesResource
```

## <span data-ttu-id="ae3ca-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="ae3ca-114">PARAMETERS</span></span>

### <span data-ttu-id="ae3ca-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="ae3ca-115">-AccountName</span></span>
<span data-ttu-id="ae3ca-116">Name des Datenbankkontos "Cosmos DB".</span><span class="sxs-lookup"><span data-stu-id="ae3ca-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="ae3ca-117">-AnalyticalStorageTtl</span><span class="sxs-lookup"><span data-stu-id="ae3ca-117">-AnalyticalStorageTtl</span></span>
<span data-ttu-id="ae3ca-118">TTL für analytische Speicherung (in Sekunden).</span><span class="sxs-lookup"><span data-stu-id="ae3ca-118">TTL for Analytical Storage (in Seconds).</span></span>

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

### <span data-ttu-id="ae3ca-119">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="ae3ca-119">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="ae3ca-120">Maximaler Durchsatzwert, wenn die automatische Skalierung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="ae3ca-120">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="ae3ca-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ae3ca-121">-Confirm</span></span>
<span data-ttu-id="ae3ca-122">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ae3ca-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae3ca-123">-ConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="ae3ca-123">-ConflictResolutionPolicy</span></span>
<span data-ttu-id="ae3ca-124">ConflictResolutionPolicy-Objekt vom Typ PSSqlConflictResolutionPolicy, sofern dies als ConflictResolutionPolicy des Containers festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="ae3ca-124">ConflictResolutionPolicy Object of type PSSqlConflictResolutionPolicy, when provided this is set as the ConflictResolutionPolicy of the container.</span></span>

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

### <span data-ttu-id="ae3ca-125">-ConflictResolutionPolicyMode</span><span class="sxs-lookup"><span data-stu-id="ae3ca-125">-ConflictResolutionPolicyMode</span></span>
<span data-ttu-id="ae3ca-126">Kann die Werte haben: LastWriterWins, Custom, Manual.</span><span class="sxs-lookup"><span data-stu-id="ae3ca-126">Can have the values: LastWriterWins, Custom, Manual.</span></span>
<span data-ttu-id="ae3ca-127">Wenn dieser Parameter zusammen mit dem Parameter ConflictResolutionPolicy bereitgestellt wird, wird er ignoriert.</span><span class="sxs-lookup"><span data-stu-id="ae3ca-127">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

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

### <span data-ttu-id="ae3ca-128">-ConflictResolutionPolicyPath</span><span class="sxs-lookup"><span data-stu-id="ae3ca-128">-ConflictResolutionPolicyPath</span></span>
<span data-ttu-id="ae3ca-129">Wird bereitgestellt, wenn der Typ LastWriterWins ist.</span><span class="sxs-lookup"><span data-stu-id="ae3ca-129">To be provided when the type is LastWriterWins.</span></span>
<span data-ttu-id="ae3ca-130">Wenn dieser Parameter zusammen mit dem Parameter ConflictResolutionPolicy bereitgestellt wird, wird er ignoriert.</span><span class="sxs-lookup"><span data-stu-id="ae3ca-130">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

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

### <span data-ttu-id="ae3ca-131">-ConflictResolutionPolicyProcedure</span><span class="sxs-lookup"><span data-stu-id="ae3ca-131">-ConflictResolutionPolicyProcedure</span></span>
<span data-ttu-id="ae3ca-132">Soll bereitgestellt werden, wenn der Typ benutzerdefinierter ist.</span><span class="sxs-lookup"><span data-stu-id="ae3ca-132">To be provided when the type is custom.</span></span>
<span data-ttu-id="ae3ca-133">Wenn dieser Parameter zusammen mit dem Parameter ConflictResolutionPolicy bereitgestellt wird, wird er ignoriert.</span><span class="sxs-lookup"><span data-stu-id="ae3ca-133">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

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

### <span data-ttu-id="ae3ca-134">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ae3ca-134">-DatabaseName</span></span>
<span data-ttu-id="ae3ca-135">Datenbankname.</span><span class="sxs-lookup"><span data-stu-id="ae3ca-135">Database name.</span></span>

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

### <span data-ttu-id="ae3ca-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae3ca-136">-DefaultProfile</span></span>
<span data-ttu-id="ae3ca-137">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ae3ca-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ae3ca-138">-IndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="ae3ca-138">-IndexingPolicy</span></span>
<span data-ttu-id="ae3ca-139">Indizierungsrichtlinienobjekt vom Typ Microsoft.Azure.Commands.CosmosDB.PSSqlIndexingPolicy.</span><span class="sxs-lookup"><span data-stu-id="ae3ca-139">Indexing Policy Object of type Microsoft.Azure.Commands.CosmosDB.PSSqlIndexingPolicy.</span></span>

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

### <span data-ttu-id="ae3ca-140">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ae3ca-140">-InputObject</span></span>
<span data-ttu-id="ae3ca-141">Sql Container-Objekt.</span><span class="sxs-lookup"><span data-stu-id="ae3ca-141">Sql Container object.</span></span>

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

### <span data-ttu-id="ae3ca-142">-Name</span><span class="sxs-lookup"><span data-stu-id="ae3ca-142">-Name</span></span>
<span data-ttu-id="ae3ca-143">Containername.</span><span class="sxs-lookup"><span data-stu-id="ae3ca-143">Container name.</span></span>

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

### <span data-ttu-id="ae3ca-144">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="ae3ca-144">-ParentObject</span></span>
<span data-ttu-id="ae3ca-145">Sql Database-Objekt.</span><span class="sxs-lookup"><span data-stu-id="ae3ca-145">Sql Database object.</span></span>

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

### <span data-ttu-id="ae3ca-146">-PartitionKeyKind</span><span class="sxs-lookup"><span data-stu-id="ae3ca-146">-PartitionKeyKind</span></span>
<span data-ttu-id="ae3ca-147">Die Art des Algorithmus, der für die Partitionierung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ae3ca-147">The kind of algorithm used for partitioning.</span></span>
<span data-ttu-id="ae3ca-148">Mögliche Werte sind: "Hash", "Bereich"</span><span class="sxs-lookup"><span data-stu-id="ae3ca-148">Possible values include: 'Hash', 'Range'</span></span>

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

### <span data-ttu-id="ae3ca-149">-PartitionKeyPath</span><span class="sxs-lookup"><span data-stu-id="ae3ca-149">-PartitionKeyPath</span></span>
<span data-ttu-id="ae3ca-150">Partition Key Path, z. B. "/address/zipcode".</span><span class="sxs-lookup"><span data-stu-id="ae3ca-150">Partition Key Path, e.g., '/address/zipcode'.</span></span>

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

### <span data-ttu-id="ae3ca-151">-PartitionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="ae3ca-151">-PartitionKeyVersion</span></span>
<span data-ttu-id="ae3ca-152">Die Version der Partitionsschlüsseldefinition</span><span class="sxs-lookup"><span data-stu-id="ae3ca-152">The version of the partition key definition</span></span>

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

### <span data-ttu-id="ae3ca-153">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae3ca-153">-ResourceGroupName</span></span>
<span data-ttu-id="ae3ca-154">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="ae3ca-154">Name of resource group.</span></span>

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

### <span data-ttu-id="ae3ca-155">-Durchsatz</span><span class="sxs-lookup"><span data-stu-id="ae3ca-155">-Throughput</span></span>
<span data-ttu-id="ae3ca-156">Der Durchsatz SQL Container (RU/s).</span><span class="sxs-lookup"><span data-stu-id="ae3ca-156">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="ae3ca-157">Der Standardwert ist 400.</span><span class="sxs-lookup"><span data-stu-id="ae3ca-157">Default value is 400.</span></span>

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

### <span data-ttu-id="ae3ca-158">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="ae3ca-158">-TtlInSeconds</span></span>
<span data-ttu-id="ae3ca-159">Standard-Ttl in Sekunden.</span><span class="sxs-lookup"><span data-stu-id="ae3ca-159">Default Ttl in seconds.</span></span>
<span data-ttu-id="ae3ca-160">Wenn der Wert fehlt oder auf - 1 festgelegt ist, laufen die Elemente nicht ab.</span><span class="sxs-lookup"><span data-stu-id="ae3ca-160">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="ae3ca-161">Wenn der Wert auf n festgelegt ist, laufen Elemente n Sekunden nach der letzten Änderungszeit ab.</span><span class="sxs-lookup"><span data-stu-id="ae3ca-161">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="ae3ca-162">-UniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="ae3ca-162">-UniqueKeyPolicy</span></span>
<span data-ttu-id="ae3ca-163">UniqueKeyPolicy-Objekt vom Typ Microsoft.Azure.Commands.CosmosDB.PSSqlUniqueKeyPolicy.</span><span class="sxs-lookup"><span data-stu-id="ae3ca-163">UniqueKeyPolicy Object of type Microsoft.Azure.Commands.CosmosDB.PSSqlUniqueKeyPolicy.</span></span>

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

### <span data-ttu-id="ae3ca-164">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae3ca-164">-WhatIf</span></span>
<span data-ttu-id="ae3ca-165">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ae3ca-165">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ae3ca-166">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ae3ca-166">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae3ca-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae3ca-167">CommonParameters</span></span>
<span data-ttu-id="ae3ca-168">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae3ca-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae3ca-169">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ae3ca-169">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae3ca-170">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ae3ca-170">INPUTS</span></span>

### <span data-ttu-id="ae3ca-171">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="ae3ca-171">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlIndexingPolicy</span></span>

### <span data-ttu-id="ae3ca-172">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="ae3ca-172">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKeyPolicy</span></span>

### <span data-ttu-id="ae3ca-173">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="ae3ca-173">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlConflictResolutionPolicy</span></span>

### <span data-ttu-id="ae3ca-174">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="ae3ca-174">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="ae3ca-175">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="ae3ca-175">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

## <span data-ttu-id="ae3ca-176">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ae3ca-176">OUTPUTS</span></span>

### <span data-ttu-id="ae3ca-177">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="ae3ca-177">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="ae3ca-178">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="ae3ca-178">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="ae3ca-179">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="ae3ca-179">NOTES</span></span>

## <span data-ttu-id="ae3ca-180">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="ae3ca-180">RELATED LINKS</span></span>
