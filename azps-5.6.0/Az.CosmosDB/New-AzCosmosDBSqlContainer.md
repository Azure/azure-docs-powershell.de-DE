---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbsqlcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlContainer.md
ms.openlocfilehash: 4fc4bd816511132d5a4fd5d317069e3baf9d9225
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101925960"
---
# <span data-ttu-id="311af-101">New-AzCosmosDBSqlContainer</span><span class="sxs-lookup"><span data-stu-id="311af-101">New-AzCosmosDBSqlContainer</span></span>

## <span data-ttu-id="311af-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="311af-102">SYNOPSIS</span></span>
<span data-ttu-id="311af-103">Erstellt einen neuen CosmosDB Sql Container.</span><span class="sxs-lookup"><span data-stu-id="311af-103">Creates a new CosmosDB Sql Container.</span></span>

## <span data-ttu-id="311af-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="311af-104">SYNTAX</span></span>

### <span data-ttu-id="311af-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="311af-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBSqlContainer -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-IndexingPolicy <PSSqlIndexingPolicy>] [-PartitionKeyVersion <Int32>]
 -PartitionKeyKind <String> -PartitionKeyPath <String[]> [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>] [-UniqueKeyPolicy <PSSqlUniqueKeyPolicy>]
 [-ConflictResolutionPolicyMode <String>] [-ConflictResolutionPolicyPath <String>]
 [-ConflictResolutionPolicyProcedure <String>] [-ConflictResolutionPolicy <PSSqlConflictResolutionPolicy>]
 [-AnalyticalStorageTtl <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="311af-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="311af-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBSqlContainer -Name <String> [-IndexingPolicy <PSSqlIndexingPolicy>]
 [-PartitionKeyVersion <Int32>] -PartitionKeyKind <String> -PartitionKeyPath <String[]> [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>] [-UniqueKeyPolicy <PSSqlUniqueKeyPolicy>]
 [-ConflictResolutionPolicyMode <String>] [-ConflictResolutionPolicyPath <String>]
 [-ConflictResolutionPolicyProcedure <String>] [-ConflictResolutionPolicy <PSSqlConflictResolutionPolicy>]
 [-AnalyticalStorageTtl <Int32>] -ParentObject <PSSqlDatabaseGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="311af-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="311af-107">DESCRIPTION</span></span>
<span data-ttu-id="311af-108">Erstellt einen neuen CosmosDB Sql Container.</span><span class="sxs-lookup"><span data-stu-id="311af-108">Creates a new CosmosDB Sql Container.</span></span>

## <span data-ttu-id="311af-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="311af-109">EXAMPLES</span></span>

### <span data-ttu-id="311af-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="311af-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlContainer -AccountName myAccountName -DatabaseName myDatabaseName -ResourceGroupName myRgName -Name myContainerName -PartitionKeyPath /a/b/c -PartitionKeyKind Hash

Name     : myContainerName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/sqlDatabases/myDatabaseName/contain
           ers/myContainerName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetPropertiesResource
```

## <span data-ttu-id="311af-111">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="311af-111">PARAMETERS</span></span>

### <span data-ttu-id="311af-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="311af-112">-AccountName</span></span>
<span data-ttu-id="311af-113">Name des Datenbankkontos "Cosmos DB".</span><span class="sxs-lookup"><span data-stu-id="311af-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="311af-114">-AnalyticalStorageTtl</span><span class="sxs-lookup"><span data-stu-id="311af-114">-AnalyticalStorageTtl</span></span>
<span data-ttu-id="311af-115">TTL für analytische Speicherung (in Sekunden).</span><span class="sxs-lookup"><span data-stu-id="311af-115">TTL for Analytical Storage (in Seconds).</span></span>

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

### <span data-ttu-id="311af-116">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="311af-116">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="311af-117">Maximaler Durchsatzwert, wenn die automatische Skalierung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="311af-117">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="311af-118">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="311af-118">-Confirm</span></span>
<span data-ttu-id="311af-119">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="311af-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="311af-120">-ConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="311af-120">-ConflictResolutionPolicy</span></span>
<span data-ttu-id="311af-121">ConflictResolutionPolicy-Objekt vom Typ PSSqlConflictResolutionPolicy, sofern dies als ConflictResolutionPolicy des Containers festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="311af-121">ConflictResolutionPolicy Object of type PSSqlConflictResolutionPolicy, when provided this is set as the ConflictResolutionPolicy of the container.</span></span>

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

### <span data-ttu-id="311af-122">-ConflictResolutionPolicyMode</span><span class="sxs-lookup"><span data-stu-id="311af-122">-ConflictResolutionPolicyMode</span></span>
<span data-ttu-id="311af-123">Kann die Werte haben: LastWriterWins, Custom, Manual.</span><span class="sxs-lookup"><span data-stu-id="311af-123">Can have the values: LastWriterWins, Custom, Manual.</span></span>
<span data-ttu-id="311af-124">Wenn dieser Parameter zusammen mit dem Parameter ConflictResolutionPolicy bereitgestellt wird, wird er ignoriert.</span><span class="sxs-lookup"><span data-stu-id="311af-124">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

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

### <span data-ttu-id="311af-125">-ConflictResolutionPolicyPath</span><span class="sxs-lookup"><span data-stu-id="311af-125">-ConflictResolutionPolicyPath</span></span>
<span data-ttu-id="311af-126">Wird bereitgestellt, wenn der Typ LastWriterWins ist.</span><span class="sxs-lookup"><span data-stu-id="311af-126">To be provided when the type is LastWriterWins.</span></span>
<span data-ttu-id="311af-127">Wenn dieser Parameter zusammen mit dem Parameter ConflictResolutionPolicy bereitgestellt wird, wird er ignoriert.</span><span class="sxs-lookup"><span data-stu-id="311af-127">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

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

### <span data-ttu-id="311af-128">-ConflictResolutionPolicyProcedure</span><span class="sxs-lookup"><span data-stu-id="311af-128">-ConflictResolutionPolicyProcedure</span></span>
<span data-ttu-id="311af-129">Soll bereitgestellt werden, wenn der Typ benutzerdefinierter ist.</span><span class="sxs-lookup"><span data-stu-id="311af-129">To be provided when the type is custom.</span></span>
<span data-ttu-id="311af-130">Wenn dieser Parameter zusammen mit dem Parameter ConflictResolutionPolicy bereitgestellt wird, wird er ignoriert.</span><span class="sxs-lookup"><span data-stu-id="311af-130">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

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

### <span data-ttu-id="311af-131">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="311af-131">-DatabaseName</span></span>
<span data-ttu-id="311af-132">Datenbankname.</span><span class="sxs-lookup"><span data-stu-id="311af-132">Database name.</span></span>

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

### <span data-ttu-id="311af-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="311af-133">-DefaultProfile</span></span>
<span data-ttu-id="311af-134">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="311af-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="311af-135">-IndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="311af-135">-IndexingPolicy</span></span>
<span data-ttu-id="311af-136">Indizierungsrichtlinienobjekt vom Typ Microsoft.Azure.Commands.CosmosDB.PSSqlIndexingPolicy.</span><span class="sxs-lookup"><span data-stu-id="311af-136">Indexing Policy Object of type Microsoft.Azure.Commands.CosmosDB.PSSqlIndexingPolicy.</span></span>

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

### <span data-ttu-id="311af-137">-Name</span><span class="sxs-lookup"><span data-stu-id="311af-137">-Name</span></span>
<span data-ttu-id="311af-138">Containername.</span><span class="sxs-lookup"><span data-stu-id="311af-138">Container name.</span></span>

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

### <span data-ttu-id="311af-139">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="311af-139">-ParentObject</span></span>
<span data-ttu-id="311af-140">Sql Database-Objekt.</span><span class="sxs-lookup"><span data-stu-id="311af-140">Sql Database object.</span></span>

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

### <span data-ttu-id="311af-141">-PartitionKeyKind</span><span class="sxs-lookup"><span data-stu-id="311af-141">-PartitionKeyKind</span></span>
<span data-ttu-id="311af-142">Die Art des Algorithmus, der für die Partitionierung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="311af-142">The kind of algorithm used for partitioning.</span></span>
<span data-ttu-id="311af-143">Mögliche Werte sind: "Hash", "Bereich"</span><span class="sxs-lookup"><span data-stu-id="311af-143">Possible values include: 'Hash', 'Range'</span></span>

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

### <span data-ttu-id="311af-144">-PartitionKeyPath</span><span class="sxs-lookup"><span data-stu-id="311af-144">-PartitionKeyPath</span></span>
<span data-ttu-id="311af-145">Partition Key Path, z. B. "/address/zipcode".</span><span class="sxs-lookup"><span data-stu-id="311af-145">Partition Key Path, e.g., '/address/zipcode'.</span></span>

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

### <span data-ttu-id="311af-146">-PartitionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="311af-146">-PartitionKeyVersion</span></span>
<span data-ttu-id="311af-147">Die Version der Partitionsschlüsseldefinition</span><span class="sxs-lookup"><span data-stu-id="311af-147">The version of the partition key definition</span></span>

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

### <span data-ttu-id="311af-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="311af-148">-ResourceGroupName</span></span>
<span data-ttu-id="311af-149">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="311af-149">Name of resource group.</span></span>

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

### <span data-ttu-id="311af-150">-Durchsatz</span><span class="sxs-lookup"><span data-stu-id="311af-150">-Throughput</span></span>
<span data-ttu-id="311af-151">Der Durchsatz SQL Container (RU/s).</span><span class="sxs-lookup"><span data-stu-id="311af-151">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="311af-152">Der Standardwert ist 400.</span><span class="sxs-lookup"><span data-stu-id="311af-152">Default value is 400.</span></span>

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

### <span data-ttu-id="311af-153">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="311af-153">-TtlInSeconds</span></span>
<span data-ttu-id="311af-154">Standard-Ttl in Sekunden.</span><span class="sxs-lookup"><span data-stu-id="311af-154">Default Ttl in seconds.</span></span>
<span data-ttu-id="311af-155">Wenn der Wert fehlt oder auf - 1 festgelegt ist, laufen die Elemente nicht ab.</span><span class="sxs-lookup"><span data-stu-id="311af-155">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="311af-156">Wenn der Wert auf n festgelegt ist, laufen Elemente n Sekunden nach der letzten Änderungszeit ab.</span><span class="sxs-lookup"><span data-stu-id="311af-156">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="311af-157">-UniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="311af-157">-UniqueKeyPolicy</span></span>
<span data-ttu-id="311af-158">UniqueKeyPolicy-Objekt vom Typ Microsoft.Azure.Commands.CosmosDB.PSSqlUniqueKeyPolicy.</span><span class="sxs-lookup"><span data-stu-id="311af-158">UniqueKeyPolicy Object of type Microsoft.Azure.Commands.CosmosDB.PSSqlUniqueKeyPolicy.</span></span>

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

### <span data-ttu-id="311af-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="311af-159">-WhatIf</span></span>
<span data-ttu-id="311af-160">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="311af-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="311af-161">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="311af-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="311af-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="311af-162">CommonParameters</span></span>
<span data-ttu-id="311af-163">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="311af-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="311af-164">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="311af-164">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="311af-165">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="311af-165">INPUTS</span></span>

### <span data-ttu-id="311af-166">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="311af-166">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlIndexingPolicy</span></span>

### <span data-ttu-id="311af-167">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="311af-167">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKeyPolicy</span></span>

### <span data-ttu-id="311af-168">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="311af-168">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlConflictResolutionPolicy</span></span>

### <span data-ttu-id="311af-169">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="311af-169">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

## <span data-ttu-id="311af-170">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="311af-170">OUTPUTS</span></span>

### <span data-ttu-id="311af-171">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="311af-171">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="311af-172">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="311af-172">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="311af-173">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="311af-173">NOTES</span></span>

## <span data-ttu-id="311af-174">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="311af-174">RELATED LINKS</span></span>
