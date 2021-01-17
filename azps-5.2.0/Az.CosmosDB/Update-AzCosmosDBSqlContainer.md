---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbsqlcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlContainer.md
ms.openlocfilehash: 85f220c7745f28a2786e9a26edc86baa129c3c3c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98371718"
---
# <span data-ttu-id="fc4ae-101">Update-AzCosmosDBSqlContainer</span><span class="sxs-lookup"><span data-stu-id="fc4ae-101">Update-AzCosmosDBSqlContainer</span></span>

## <span data-ttu-id="fc4ae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fc4ae-102">SYNOPSIS</span></span>
<span data-ttu-id="fc4ae-103">Aktualisiert den Sql-Container".</span><span class="sxs-lookup"><span data-stu-id="fc4ae-103">Updates the CosmosDB Sql Container.</span></span> <span data-ttu-id="fc4ae-104">Führt einen clientseitigen Patchvorgang durch, indem der vorhandene Container gelesen wird.</span><span class="sxs-lookup"><span data-stu-id="fc4ae-104">Performs a client side patch operation by reading the existing Container.</span></span>

## <span data-ttu-id="fc4ae-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fc4ae-105">SYNTAX</span></span>

### <span data-ttu-id="fc4ae-106">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="fc4ae-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBSqlContainer -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 [-Name <String>] [-IndexingPolicy <PSSqlIndexingPolicy>] [-PartitionKeyVersion <Int32>]
 [-PartitionKeyKind <String>] [-PartitionKeyPath <String[]>] [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>] [-UniqueKeyPolicy <PSSqlUniqueKeyPolicy>]
 [-ConflictResolutionPolicyMode <String>] [-ConflictResolutionPolicyPath <String>]
 [-ConflictResolutionPolicyProcedure <String>] [-ConflictResolutionPolicy <PSSqlConflictResolutionPolicy>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc4ae-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fc4ae-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlContainer [-Name <String>] [-IndexingPolicy <PSSqlIndexingPolicy>]
 [-PartitionKeyVersion <Int32>] [-PartitionKeyKind <String>] [-PartitionKeyPath <String[]>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-UniqueKeyPolicy <PSSqlUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSSqlConflictResolutionPolicy>] -ParentObject <PSSqlDatabaseGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc4ae-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fc4ae-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlContainer [-Name <String>] [-IndexingPolicy <PSSqlIndexingPolicy>]
 [-PartitionKeyVersion <Int32>] [-PartitionKeyKind <String>] [-PartitionKeyPath <String[]>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-UniqueKeyPolicy <PSSqlUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSSqlConflictResolutionPolicy>] -InputObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fc4ae-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fc4ae-109">DESCRIPTION</span></span>
<span data-ttu-id="fc4ae-110">Aktualisiert den Sql-Container".</span><span class="sxs-lookup"><span data-stu-id="fc4ae-110">Updates the CosmosDB Sql Container.</span></span> <span data-ttu-id="fc4ae-111">Führt einen clientseitigen Patchvorgang durch, indem der vorhandene Container gelesen wird.</span><span class="sxs-lookup"><span data-stu-id="fc4ae-111">Performs a client side patch operation by reading the existing Container.</span></span>

## <span data-ttu-id="fc4ae-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="fc4ae-112">EXAMPLES</span></span>

### <span data-ttu-id="fc4ae-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="fc4ae-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBMongoDBDatabase -AccountName myAccountName -Name myDatabaseName -ResourceGroupName myResourcegroupName -Throughput 800

Name     : myDatabaseName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/mongodbDatabases/myDatabaseName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetPropertiesResource
```

## <span data-ttu-id="fc4ae-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fc4ae-114">PARAMETERS</span></span>

### <span data-ttu-id="fc4ae-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="fc4ae-115">-AccountName</span></span>
<span data-ttu-id="fc4ae-116">Name des Dbdatenbankkontos".</span><span class="sxs-lookup"><span data-stu-id="fc4ae-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="fc4ae-117">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="fc4ae-117">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="fc4ae-118">Der maximale Durchsatzwert, wenn die Automatische Skalierung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="fc4ae-118">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="fc4ae-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fc4ae-119">-Confirm</span></span>
<span data-ttu-id="fc4ae-120">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="fc4ae-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fc4ae-121">-ConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="fc4ae-121">-ConflictResolutionPolicy</span></span>
<span data-ttu-id="fc4ae-122">ConflictResolutionPolicy-Objekt vom Typ PSSqlConflictResolutionPolicy, wenn dies als "ConflictResolutionPolicy" des Containers festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="fc4ae-122">ConflictResolutionPolicy Object of type PSSqlConflictResolutionPolicy, when provided this is set as the ConflictResolutionPolicy of the container.</span></span>

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

### <span data-ttu-id="fc4ae-123">-ConflictResolutionPolicyMode</span><span class="sxs-lookup"><span data-stu-id="fc4ae-123">-ConflictResolutionPolicyMode</span></span>
<span data-ttu-id="fc4ae-124">Kann die Werte haben: LastWriterWins, Custom, Manual.</span><span class="sxs-lookup"><span data-stu-id="fc4ae-124">Can have the values: LastWriterWins, Custom, Manual.</span></span>
<span data-ttu-id="fc4ae-125">Wenn diese Zusammen mit dem Parameter "ConflictResolutionPolicy" angegeben wird, wird sie ignoriert.</span><span class="sxs-lookup"><span data-stu-id="fc4ae-125">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

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

### <span data-ttu-id="fc4ae-126">-ConflictResolutionPolicyPath</span><span class="sxs-lookup"><span data-stu-id="fc4ae-126">-ConflictResolutionPolicyPath</span></span>
<span data-ttu-id="fc4ae-127">Wird bereitgestellt, wenn der Typ "LastWriterWins" ist.</span><span class="sxs-lookup"><span data-stu-id="fc4ae-127">To be provided when the type is LastWriterWins.</span></span>
<span data-ttu-id="fc4ae-128">Wenn diese Zusammen mit dem Parameter "ConflictResolutionPolicy" angegeben wird, wird sie ignoriert.</span><span class="sxs-lookup"><span data-stu-id="fc4ae-128">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

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

### <span data-ttu-id="fc4ae-129">-ConflictResolutionPolicyProcedure</span><span class="sxs-lookup"><span data-stu-id="fc4ae-129">-ConflictResolutionPolicyProcedure</span></span>
<span data-ttu-id="fc4ae-130">Wird bereitgestellt, wenn es sich um einen benutzerdefinierten Typ handelt.</span><span class="sxs-lookup"><span data-stu-id="fc4ae-130">To be provided when the type is custom.</span></span>
<span data-ttu-id="fc4ae-131">Wenn diese Zusammen mit dem Parameter "ConflictResolutionPolicy" angegeben wird, wird sie ignoriert.</span><span class="sxs-lookup"><span data-stu-id="fc4ae-131">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

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

### <span data-ttu-id="fc4ae-132">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="fc4ae-132">-DatabaseName</span></span>
<span data-ttu-id="fc4ae-133">Datenbankname.</span><span class="sxs-lookup"><span data-stu-id="fc4ae-133">Database name.</span></span>

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

### <span data-ttu-id="fc4ae-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc4ae-134">-DefaultProfile</span></span>
<span data-ttu-id="fc4ae-135">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fc4ae-135">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fc4ae-136">-IndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="fc4ae-136">-IndexingPolicy</span></span>
<span data-ttu-id="fc4ae-137">Indizierungsrichtlinienobjekt vom Typ "Microsoft.Azure.Commands.UmsDB.PSSqlIndexingPolicy".</span><span class="sxs-lookup"><span data-stu-id="fc4ae-137">Indexing Policy Object of type Microsoft.Azure.Commands.CosmosDB.PSSqlIndexingPolicy.</span></span>

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

### <span data-ttu-id="fc4ae-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fc4ae-138">-InputObject</span></span>
<span data-ttu-id="fc4ae-139">Sql Container-Objekt.</span><span class="sxs-lookup"><span data-stu-id="fc4ae-139">Sql Container object.</span></span>

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

### <span data-ttu-id="fc4ae-140">-Name</span><span class="sxs-lookup"><span data-stu-id="fc4ae-140">-Name</span></span>
<span data-ttu-id="fc4ae-141">Containername.</span><span class="sxs-lookup"><span data-stu-id="fc4ae-141">Container name.</span></span>

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

### <span data-ttu-id="fc4ae-142">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="fc4ae-142">-ParentObject</span></span>
<span data-ttu-id="fc4ae-143">Sql-Datenbankobjekt.</span><span class="sxs-lookup"><span data-stu-id="fc4ae-143">Sql Database object.</span></span>

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

### <span data-ttu-id="fc4ae-144">-PartitionKeyKind</span><span class="sxs-lookup"><span data-stu-id="fc4ae-144">-PartitionKeyKind</span></span>
<span data-ttu-id="fc4ae-145">Die Art des Algorithmus, der für die Partitionierung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="fc4ae-145">The kind of algorithm used for partitioning.</span></span>
<span data-ttu-id="fc4ae-146">Mögliche Werte sind: 'Hash', 'Range'</span><span class="sxs-lookup"><span data-stu-id="fc4ae-146">Possible values include: 'Hash', 'Range'</span></span>

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

### <span data-ttu-id="fc4ae-147">-PartitionKeyPath</span><span class="sxs-lookup"><span data-stu-id="fc4ae-147">-PartitionKeyPath</span></span>
<span data-ttu-id="fc4ae-148">Partition Key Path, z. B. '/address/zipcode'.</span><span class="sxs-lookup"><span data-stu-id="fc4ae-148">Partition Key Path, e.g., '/address/zipcode'.</span></span>

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

### <span data-ttu-id="fc4ae-149">-PartitionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="fc4ae-149">-PartitionKeyVersion</span></span>
<span data-ttu-id="fc4ae-150">Die Version der Definition des Partitionsschlüssels</span><span class="sxs-lookup"><span data-stu-id="fc4ae-150">The version of the partition key definition</span></span>

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

### <span data-ttu-id="fc4ae-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc4ae-151">-ResourceGroupName</span></span>
<span data-ttu-id="fc4ae-152">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="fc4ae-152">Name of resource group.</span></span>

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

### <span data-ttu-id="fc4ae-153">-Throughput</span><span class="sxs-lookup"><span data-stu-id="fc4ae-153">-Throughput</span></span>
<span data-ttu-id="fc4ae-154">Der Durchsatz SQL Container (RU/s).</span><span class="sxs-lookup"><span data-stu-id="fc4ae-154">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="fc4ae-155">Der Standardwert ist 400.</span><span class="sxs-lookup"><span data-stu-id="fc4ae-155">Default value is 400.</span></span>

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

### <span data-ttu-id="fc4ae-156">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="fc4ae-156">-TtlInSeconds</span></span>
<span data-ttu-id="fc4ae-157">Standard-Ttl in Sekunden.</span><span class="sxs-lookup"><span data-stu-id="fc4ae-157">Default Ttl in seconds.</span></span>
<span data-ttu-id="fc4ae-158">Wenn der Wert fehlt oder auf -1 festgelegt ist, laufen die Elemente nicht ab.</span><span class="sxs-lookup"><span data-stu-id="fc4ae-158">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="fc4ae-159">Wenn der Wert auf "n" festgelegt ist, laufen die Elemente n Sekunden nach der letzten Änderung ab.</span><span class="sxs-lookup"><span data-stu-id="fc4ae-159">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="fc4ae-160">-UniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="fc4ae-160">-UniqueKeyPolicy</span></span>
<span data-ttu-id="fc4ae-161">"UniqueKeyPolicy"-Objekt vom Typ "Microsoft.Azure.Commands.UmsDB.PSSqlUniqueKeyPolicy".</span><span class="sxs-lookup"><span data-stu-id="fc4ae-161">UniqueKeyPolicy Object of type Microsoft.Azure.Commands.CosmosDB.PSSqlUniqueKeyPolicy.</span></span>

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

### <span data-ttu-id="fc4ae-162">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="fc4ae-162">-WhatIf</span></span>
<span data-ttu-id="fc4ae-163">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fc4ae-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fc4ae-164">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fc4ae-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fc4ae-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc4ae-165">CommonParameters</span></span>
<span data-ttu-id="fc4ae-166">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc4ae-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc4ae-167">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fc4ae-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc4ae-168">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="fc4ae-168">INPUTS</span></span>

### <span data-ttu-id="fc4ae-169">Microsoft.Azure.Commands.SkriptsDB.Models.PSSqlIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="fc4ae-169">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlIndexingPolicy</span></span>

### <span data-ttu-id="fc4ae-170">Microsoft.Azure.Commands.SkriptsDB.Models.PSSqlUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="fc4ae-170">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKeyPolicy</span></span>

### <span data-ttu-id="fc4ae-171">Microsoft.Azure.Commands.SkriptsDB.Models.PSSqlConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="fc4ae-171">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlConflictResolutionPolicy</span></span>

### <span data-ttu-id="fc4ae-172">Microsoft.Azure.Commands.ExesDB.Models.PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="fc4ae-172">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="fc4ae-173">Microsoft.Azure.Commands.ExesDB.Models.PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="fc4ae-173">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

## <span data-ttu-id="fc4ae-174">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="fc4ae-174">OUTPUTS</span></span>

### <span data-ttu-id="fc4ae-175">Microsoft.Azure.Commands.ExesDB.Models.PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="fc4ae-175">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="fc4ae-176">Microsoft.Azure.Commands.UmsDB.Exceptions.ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="fc4ae-176">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="fc4ae-177">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="fc4ae-177">NOTES</span></span>

## <span data-ttu-id="fc4ae-178">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="fc4ae-178">RELATED LINKS</span></span>
