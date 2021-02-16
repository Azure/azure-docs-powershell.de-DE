---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbsqlcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlContainer.md
ms.openlocfilehash: 60bbe085aaaa65c65ba33839db5f02ae5198e155
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100148473"
---
# <span data-ttu-id="174a0-101">Update-AzCosmosDBSqlContainer</span><span class="sxs-lookup"><span data-stu-id="174a0-101">Update-AzCosmosDBSqlContainer</span></span>

## <span data-ttu-id="174a0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="174a0-102">SYNOPSIS</span></span>
<span data-ttu-id="174a0-103">Aktualisiert den Sql-Container".</span><span class="sxs-lookup"><span data-stu-id="174a0-103">Updates the CosmosDB Sql Container.</span></span> <span data-ttu-id="174a0-104">Führt einen clientseitigen Patchvorgang durch, indem der vorhandene Container gelesen wird.</span><span class="sxs-lookup"><span data-stu-id="174a0-104">Performs a client side patch operation by reading the existing Container.</span></span>

## <span data-ttu-id="174a0-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="174a0-105">SYNTAX</span></span>

### <span data-ttu-id="174a0-106">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="174a0-106">ByNameParameterSet (Default)</span></span>
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

### <span data-ttu-id="174a0-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="174a0-107">ByParentObjectParameterSet</span></span>
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

### <span data-ttu-id="174a0-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="174a0-108">ByObjectParameterSet</span></span>
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

## <span data-ttu-id="174a0-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="174a0-109">DESCRIPTION</span></span>
<span data-ttu-id="174a0-110">Aktualisiert den Sql-Container".</span><span class="sxs-lookup"><span data-stu-id="174a0-110">Updates the CosmosDB Sql Container.</span></span> <span data-ttu-id="174a0-111">Führt einen clientseitigen Patchvorgang durch, indem der vorhandene Container gelesen wird.</span><span class="sxs-lookup"><span data-stu-id="174a0-111">Performs a client side patch operation by reading the existing Container.</span></span>

## <span data-ttu-id="174a0-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="174a0-112">EXAMPLES</span></span>

### <span data-ttu-id="174a0-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="174a0-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBMongoDBDatabase -AccountName myAccountName -Name myDatabaseName -ResourceGroupName myResourcegroupName -Throughput 800

Name     : myDatabaseName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/mongodbDatabases/myDatabaseName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetPropertiesResource
```

## <span data-ttu-id="174a0-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="174a0-114">PARAMETERS</span></span>

### <span data-ttu-id="174a0-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="174a0-115">-AccountName</span></span>
<span data-ttu-id="174a0-116">Der Name des Dbdatenbankkontos von Db.</span><span class="sxs-lookup"><span data-stu-id="174a0-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="174a0-117">-AnalyticalStorageTtl</span><span class="sxs-lookup"><span data-stu-id="174a0-117">-AnalyticalStorageTtl</span></span>
<span data-ttu-id="174a0-118">TTL für Analysespeicher (in Sekunden).</span><span class="sxs-lookup"><span data-stu-id="174a0-118">TTL for Analytical Storage (in Seconds).</span></span>

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

### <span data-ttu-id="174a0-119">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="174a0-119">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="174a0-120">Der maximale Durchsatzwert, wenn die Automatische Skalierung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="174a0-120">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="174a0-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="174a0-121">-Confirm</span></span>
<span data-ttu-id="174a0-122">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="174a0-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="174a0-123">-ConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="174a0-123">-ConflictResolutionPolicy</span></span>
<span data-ttu-id="174a0-124">ConflictResolutionPolicy-Objekt vom Typ "PSSqlConflictResolutionPolicy", wenn dies als "ConflictResolutionPolicy" des Containers festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="174a0-124">ConflictResolutionPolicy Object of type PSSqlConflictResolutionPolicy, when provided this is set as the ConflictResolutionPolicy of the container.</span></span>

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

### <span data-ttu-id="174a0-125">-ConflictResolutionPolicyMode</span><span class="sxs-lookup"><span data-stu-id="174a0-125">-ConflictResolutionPolicyMode</span></span>
<span data-ttu-id="174a0-126">Kann die Werte haben: LastWriterWins, Custom, Manual.</span><span class="sxs-lookup"><span data-stu-id="174a0-126">Can have the values: LastWriterWins, Custom, Manual.</span></span>
<span data-ttu-id="174a0-127">Wenn diese Zusammen mit dem Parameter "ConflictResolutionPolicy" angegeben wird, wird sie ignoriert.</span><span class="sxs-lookup"><span data-stu-id="174a0-127">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

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

### <span data-ttu-id="174a0-128">-ConflictResolutionPolicyPath</span><span class="sxs-lookup"><span data-stu-id="174a0-128">-ConflictResolutionPolicyPath</span></span>
<span data-ttu-id="174a0-129">Wird bereitgestellt, wenn der Typ "LastWriterWins" ist.</span><span class="sxs-lookup"><span data-stu-id="174a0-129">To be provided when the type is LastWriterWins.</span></span>
<span data-ttu-id="174a0-130">Wenn diese Zusammen mit dem Parameter "ConflictResolutionPolicy" angegeben wird, wird sie ignoriert.</span><span class="sxs-lookup"><span data-stu-id="174a0-130">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

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

### <span data-ttu-id="174a0-131">-ConflictResolutionPolicyProcedure</span><span class="sxs-lookup"><span data-stu-id="174a0-131">-ConflictResolutionPolicyProcedure</span></span>
<span data-ttu-id="174a0-132">Wird bereitgestellt, wenn es sich um einen benutzerdefinierten Typ handelt.</span><span class="sxs-lookup"><span data-stu-id="174a0-132">To be provided when the type is custom.</span></span>
<span data-ttu-id="174a0-133">Wenn diese Zusammen mit dem Parameter "ConflictResolutionPolicy" angegeben wird, wird sie ignoriert.</span><span class="sxs-lookup"><span data-stu-id="174a0-133">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

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

### <span data-ttu-id="174a0-134">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="174a0-134">-DatabaseName</span></span>
<span data-ttu-id="174a0-135">Datenbankname.</span><span class="sxs-lookup"><span data-stu-id="174a0-135">Database name.</span></span>

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

### <span data-ttu-id="174a0-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="174a0-136">-DefaultProfile</span></span>
<span data-ttu-id="174a0-137">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="174a0-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="174a0-138">-IndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="174a0-138">-IndexingPolicy</span></span>
<span data-ttu-id="174a0-139">Indizierungsrichtlinienobjekt vom Typ "Microsoft.Azure.Commands.UmsDB.PSSqlIndexingPolicy".</span><span class="sxs-lookup"><span data-stu-id="174a0-139">Indexing Policy Object of type Microsoft.Azure.Commands.CosmosDB.PSSqlIndexingPolicy.</span></span>

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

### <span data-ttu-id="174a0-140">-InputObject</span><span class="sxs-lookup"><span data-stu-id="174a0-140">-InputObject</span></span>
<span data-ttu-id="174a0-141">Sql Container-Objekt.</span><span class="sxs-lookup"><span data-stu-id="174a0-141">Sql Container object.</span></span>

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

### <span data-ttu-id="174a0-142">-Name</span><span class="sxs-lookup"><span data-stu-id="174a0-142">-Name</span></span>
<span data-ttu-id="174a0-143">Containername.</span><span class="sxs-lookup"><span data-stu-id="174a0-143">Container name.</span></span>

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

### <span data-ttu-id="174a0-144">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="174a0-144">-ParentObject</span></span>
<span data-ttu-id="174a0-145">Sql-Datenbankobjekt.</span><span class="sxs-lookup"><span data-stu-id="174a0-145">Sql Database object.</span></span>

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

### <span data-ttu-id="174a0-146">-PartitionKeyKind</span><span class="sxs-lookup"><span data-stu-id="174a0-146">-PartitionKeyKind</span></span>
<span data-ttu-id="174a0-147">Die Art des Algorithmus, der für die Partitionierung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="174a0-147">The kind of algorithm used for partitioning.</span></span>
<span data-ttu-id="174a0-148">Mögliche Werte sind: 'Hash', 'Range'</span><span class="sxs-lookup"><span data-stu-id="174a0-148">Possible values include: 'Hash', 'Range'</span></span>

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

### <span data-ttu-id="174a0-149">-PartitionKeyPath</span><span class="sxs-lookup"><span data-stu-id="174a0-149">-PartitionKeyPath</span></span>
<span data-ttu-id="174a0-150">Partition Key Path, z. B. '/address/zipcode'.</span><span class="sxs-lookup"><span data-stu-id="174a0-150">Partition Key Path, e.g., '/address/zipcode'.</span></span>

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

### <span data-ttu-id="174a0-151">-PartitionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="174a0-151">-PartitionKeyVersion</span></span>
<span data-ttu-id="174a0-152">Die Version der Definition des Partitionsschlüssels</span><span class="sxs-lookup"><span data-stu-id="174a0-152">The version of the partition key definition</span></span>

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

### <span data-ttu-id="174a0-153">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="174a0-153">-ResourceGroupName</span></span>
<span data-ttu-id="174a0-154">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="174a0-154">Name of resource group.</span></span>

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

### <span data-ttu-id="174a0-155">-Throughput</span><span class="sxs-lookup"><span data-stu-id="174a0-155">-Throughput</span></span>
<span data-ttu-id="174a0-156">Der Durchsatz SQL Container (RU/s).</span><span class="sxs-lookup"><span data-stu-id="174a0-156">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="174a0-157">Der Standardwert ist 400.</span><span class="sxs-lookup"><span data-stu-id="174a0-157">Default value is 400.</span></span>

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

### <span data-ttu-id="174a0-158">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="174a0-158">-TtlInSeconds</span></span>
<span data-ttu-id="174a0-159">Standard-Ttl in Sekunden.</span><span class="sxs-lookup"><span data-stu-id="174a0-159">Default Ttl in seconds.</span></span>
<span data-ttu-id="174a0-160">Wenn der Wert fehlt oder auf -1 festgelegt ist, laufen die Elemente nicht ab.</span><span class="sxs-lookup"><span data-stu-id="174a0-160">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="174a0-161">Wenn der Wert auf "n" festgelegt ist, laufen die Elemente n Sekunden nach der letzten Änderung ab.</span><span class="sxs-lookup"><span data-stu-id="174a0-161">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="174a0-162">-UniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="174a0-162">-UniqueKeyPolicy</span></span>
<span data-ttu-id="174a0-163">"UniqueKeyPolicy"-Objekt vom Typ "Microsoft.Azure.Commands.UmsDB.PSSqlUniqueKeyPolicy".</span><span class="sxs-lookup"><span data-stu-id="174a0-163">UniqueKeyPolicy Object of type Microsoft.Azure.Commands.CosmosDB.PSSqlUniqueKeyPolicy.</span></span>

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

### <span data-ttu-id="174a0-164">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="174a0-164">-WhatIf</span></span>
<span data-ttu-id="174a0-165">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="174a0-165">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="174a0-166">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="174a0-166">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="174a0-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="174a0-167">CommonParameters</span></span>
<span data-ttu-id="174a0-168">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="174a0-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="174a0-169">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="174a0-169">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="174a0-170">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="174a0-170">INPUTS</span></span>

### <span data-ttu-id="174a0-171">Microsoft.Azure.Commands.SkriptsDB.Models.PSSqlIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="174a0-171">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlIndexingPolicy</span></span>

### <span data-ttu-id="174a0-172">Microsoft.Azure.Commands.SkriptsDB.Models.PSSqlUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="174a0-172">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKeyPolicy</span></span>

### <span data-ttu-id="174a0-173">Microsoft.Azure.Commands.SkriptsDB.Models.PSSqlConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="174a0-173">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlConflictResolutionPolicy</span></span>

### <span data-ttu-id="174a0-174">Microsoft.Azure.Commands.ExesDB.Models.PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="174a0-174">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="174a0-175">Microsoft.Azure.Commands.ExesDB.Models.PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="174a0-175">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

## <span data-ttu-id="174a0-176">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="174a0-176">OUTPUTS</span></span>

### <span data-ttu-id="174a0-177">Microsoft.Azure.Commands.ExesDB.Models.PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="174a0-177">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="174a0-178">Microsoft.Azure.Commands.UmsDB.Exceptions.ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="174a0-178">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="174a0-179">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="174a0-179">NOTES</span></span>

## <span data-ttu-id="174a0-180">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="174a0-180">RELATED LINKS</span></span>
