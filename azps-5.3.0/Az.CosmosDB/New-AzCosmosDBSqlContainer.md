---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqlcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlContainer.md
ms.openlocfilehash: afdd1296b01a6798d9253b7b21d15ba66f924c34
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98470715"
---
# <span data-ttu-id="5dfce-101">New-AzCosmosDBSqlContainer</span><span class="sxs-lookup"><span data-stu-id="5dfce-101">New-AzCosmosDBSqlContainer</span></span>

## <span data-ttu-id="5dfce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5dfce-102">SYNOPSIS</span></span>
<span data-ttu-id="5dfce-103">Erstellt einen neuen Sql Container für Abendb.</span><span class="sxs-lookup"><span data-stu-id="5dfce-103">Creates a new CosmosDB Sql Container.</span></span>

## <span data-ttu-id="5dfce-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5dfce-104">SYNTAX</span></span>

### <span data-ttu-id="5dfce-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="5dfce-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBSqlContainer -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-IndexingPolicy <PSSqlIndexingPolicy>] [-PartitionKeyVersion <Int32>]
 -PartitionKeyKind <String> -PartitionKeyPath <String[]> [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>] [-UniqueKeyPolicy <PSSqlUniqueKeyPolicy>]
 [-ConflictResolutionPolicyMode <String>] [-ConflictResolutionPolicyPath <String>]
 [-ConflictResolutionPolicyProcedure <String>] [-ConflictResolutionPolicy <PSSqlConflictResolutionPolicy>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5dfce-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5dfce-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBSqlContainer -Name <String> [-IndexingPolicy <PSSqlIndexingPolicy>]
 [-PartitionKeyVersion <Int32>] -PartitionKeyKind <String> -PartitionKeyPath <String[]> [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>] [-UniqueKeyPolicy <PSSqlUniqueKeyPolicy>]
 [-ConflictResolutionPolicyMode <String>] [-ConflictResolutionPolicyPath <String>]
 [-ConflictResolutionPolicyProcedure <String>] [-ConflictResolutionPolicy <PSSqlConflictResolutionPolicy>]
 -ParentObject <PSSqlDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5dfce-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5dfce-107">DESCRIPTION</span></span>
<span data-ttu-id="5dfce-108">Erstellt einen neuen Sql Container für Abendb.</span><span class="sxs-lookup"><span data-stu-id="5dfce-108">Creates a new CosmosDB Sql Container.</span></span>

## <span data-ttu-id="5dfce-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5dfce-109">EXAMPLES</span></span>

### <span data-ttu-id="5dfce-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5dfce-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlContainer -AccountName myAccountName -DatabaseName myDatabaseName -ResourceGroupName myRgName -Name myContainerName -PartitionKeyPath /a/b/c -PartitionKeyKind Hash

Name     : myContainerName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/sqlDatabases/myDatabaseName/contain
           ers/myContainerName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetPropertiesResource
```

## <span data-ttu-id="5dfce-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5dfce-111">PARAMETERS</span></span>

### <span data-ttu-id="5dfce-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="5dfce-112">-AccountName</span></span>
<span data-ttu-id="5dfce-113">Name des Dbdatenbankkontos".</span><span class="sxs-lookup"><span data-stu-id="5dfce-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="5dfce-114">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="5dfce-114">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="5dfce-115">Der maximale Durchsatzwert, wenn die Automatische Skalierung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="5dfce-115">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="5dfce-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5dfce-116">-Confirm</span></span>
<span data-ttu-id="5dfce-117">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5dfce-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5dfce-118">-ConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="5dfce-118">-ConflictResolutionPolicy</span></span>
<span data-ttu-id="5dfce-119">ConflictResolutionPolicy-Objekt vom Typ PSSqlConflictResolutionPolicy, wenn dies als "ConflictResolutionPolicy" des Containers festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="5dfce-119">ConflictResolutionPolicy Object of type PSSqlConflictResolutionPolicy, when provided this is set as the ConflictResolutionPolicy of the container.</span></span>

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

### <span data-ttu-id="5dfce-120">-ConflictResolutionPolicyMode</span><span class="sxs-lookup"><span data-stu-id="5dfce-120">-ConflictResolutionPolicyMode</span></span>
<span data-ttu-id="5dfce-121">Kann die Werte haben: LastWriterWins, Custom, Manual.</span><span class="sxs-lookup"><span data-stu-id="5dfce-121">Can have the values: LastWriterWins, Custom, Manual.</span></span>
<span data-ttu-id="5dfce-122">Wenn diese Zusammen mit dem Parameter "ConflictResolutionPolicy" angegeben wird, wird sie ignoriert.</span><span class="sxs-lookup"><span data-stu-id="5dfce-122">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

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

### <span data-ttu-id="5dfce-123">-ConflictResolutionPolicyPath</span><span class="sxs-lookup"><span data-stu-id="5dfce-123">-ConflictResolutionPolicyPath</span></span>
<span data-ttu-id="5dfce-124">Wird bereitgestellt, wenn der Typ "LastWriterWins" ist.</span><span class="sxs-lookup"><span data-stu-id="5dfce-124">To be provided when the type is LastWriterWins.</span></span>
<span data-ttu-id="5dfce-125">Wenn diese Zusammen mit dem Parameter "ConflictResolutionPolicy" angegeben wird, wird sie ignoriert.</span><span class="sxs-lookup"><span data-stu-id="5dfce-125">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

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

### <span data-ttu-id="5dfce-126">-ConflictResolutionPolicyProcedure</span><span class="sxs-lookup"><span data-stu-id="5dfce-126">-ConflictResolutionPolicyProcedure</span></span>
<span data-ttu-id="5dfce-127">Wird bereitgestellt, wenn es sich um einen benutzerdefinierten Typ handelt.</span><span class="sxs-lookup"><span data-stu-id="5dfce-127">To be provided when the type is custom.</span></span>
<span data-ttu-id="5dfce-128">Wenn diese Zusammen mit dem Parameter "ConflictResolutionPolicy" angegeben wird, wird sie ignoriert.</span><span class="sxs-lookup"><span data-stu-id="5dfce-128">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

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

### <span data-ttu-id="5dfce-129">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="5dfce-129">-DatabaseName</span></span>
<span data-ttu-id="5dfce-130">Datenbankname.</span><span class="sxs-lookup"><span data-stu-id="5dfce-130">Database name.</span></span>

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

### <span data-ttu-id="5dfce-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5dfce-131">-DefaultProfile</span></span>
<span data-ttu-id="5dfce-132">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5dfce-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5dfce-133">-IndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="5dfce-133">-IndexingPolicy</span></span>
<span data-ttu-id="5dfce-134">Indizierungsrichtlinienobjekt vom Typ "Microsoft.Azure.Commands.UmsDB.PSSqlIndexingPolicy".</span><span class="sxs-lookup"><span data-stu-id="5dfce-134">Indexing Policy Object of type Microsoft.Azure.Commands.CosmosDB.PSSqlIndexingPolicy.</span></span>

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

### <span data-ttu-id="5dfce-135">-Name</span><span class="sxs-lookup"><span data-stu-id="5dfce-135">-Name</span></span>
<span data-ttu-id="5dfce-136">Containername.</span><span class="sxs-lookup"><span data-stu-id="5dfce-136">Container name.</span></span>

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

### <span data-ttu-id="5dfce-137">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="5dfce-137">-ParentObject</span></span>
<span data-ttu-id="5dfce-138">Sql-Datenbankobjekt.</span><span class="sxs-lookup"><span data-stu-id="5dfce-138">Sql Database object.</span></span>

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

### <span data-ttu-id="5dfce-139">-PartitionKeyKind</span><span class="sxs-lookup"><span data-stu-id="5dfce-139">-PartitionKeyKind</span></span>
<span data-ttu-id="5dfce-140">Die Art des Algorithmus, der für die Partitionierung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5dfce-140">The kind of algorithm used for partitioning.</span></span>
<span data-ttu-id="5dfce-141">Mögliche Werte sind: 'Hash', 'Range'</span><span class="sxs-lookup"><span data-stu-id="5dfce-141">Possible values include: 'Hash', 'Range'</span></span>

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

### <span data-ttu-id="5dfce-142">-PartitionKeyPath</span><span class="sxs-lookup"><span data-stu-id="5dfce-142">-PartitionKeyPath</span></span>
<span data-ttu-id="5dfce-143">Partition Key Path, z. B. '/address/zipcode'.</span><span class="sxs-lookup"><span data-stu-id="5dfce-143">Partition Key Path, e.g., '/address/zipcode'.</span></span>

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

### <span data-ttu-id="5dfce-144">-PartitionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="5dfce-144">-PartitionKeyVersion</span></span>
<span data-ttu-id="5dfce-145">Die Version der Definition des Partitionsschlüssels</span><span class="sxs-lookup"><span data-stu-id="5dfce-145">The version of the partition key definition</span></span>

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

### <span data-ttu-id="5dfce-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5dfce-146">-ResourceGroupName</span></span>
<span data-ttu-id="5dfce-147">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="5dfce-147">Name of resource group.</span></span>

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

### <span data-ttu-id="5dfce-148">-Throughput</span><span class="sxs-lookup"><span data-stu-id="5dfce-148">-Throughput</span></span>
<span data-ttu-id="5dfce-149">Der Durchsatz SQL Container (RU/s).</span><span class="sxs-lookup"><span data-stu-id="5dfce-149">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="5dfce-150">Der Standardwert ist 400.</span><span class="sxs-lookup"><span data-stu-id="5dfce-150">Default value is 400.</span></span>

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

### <span data-ttu-id="5dfce-151">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="5dfce-151">-TtlInSeconds</span></span>
<span data-ttu-id="5dfce-152">Standard-Ttl in Sekunden.</span><span class="sxs-lookup"><span data-stu-id="5dfce-152">Default Ttl in seconds.</span></span>
<span data-ttu-id="5dfce-153">Wenn der Wert fehlt oder auf -1 festgelegt ist, laufen die Elemente nicht ab.</span><span class="sxs-lookup"><span data-stu-id="5dfce-153">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="5dfce-154">Wenn der Wert auf "n" festgelegt ist, laufen die Elemente n Sekunden nach der letzten Änderung ab.</span><span class="sxs-lookup"><span data-stu-id="5dfce-154">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="5dfce-155">-UniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="5dfce-155">-UniqueKeyPolicy</span></span>
<span data-ttu-id="5dfce-156">"UniqueKeyPolicy"-Objekt vom Typ "Microsoft.Azure.Commands.UmsDB.PSSqlUniqueKeyPolicy".</span><span class="sxs-lookup"><span data-stu-id="5dfce-156">UniqueKeyPolicy Object of type Microsoft.Azure.Commands.CosmosDB.PSSqlUniqueKeyPolicy.</span></span>

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

### <span data-ttu-id="5dfce-157">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="5dfce-157">-WhatIf</span></span>
<span data-ttu-id="5dfce-158">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5dfce-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5dfce-159">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5dfce-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5dfce-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5dfce-160">CommonParameters</span></span>
<span data-ttu-id="5dfce-161">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5dfce-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5dfce-162">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5dfce-162">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5dfce-163">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5dfce-163">INPUTS</span></span>

### <span data-ttu-id="5dfce-164">Microsoft.Azure.Commands.SkriptsDB.Models.PSSqlIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="5dfce-164">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlIndexingPolicy</span></span>

### <span data-ttu-id="5dfce-165">Microsoft.Azure.Commands.SkriptsDB.Models.PSSqlUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="5dfce-165">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKeyPolicy</span></span>

### <span data-ttu-id="5dfce-166">Microsoft.Azure.Commands.SkriptsDB.Models.PSSqlConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="5dfce-166">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlConflictResolutionPolicy</span></span>

### <span data-ttu-id="5dfce-167">Microsoft.Azure.Commands.ExesDB.Models.PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="5dfce-167">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

## <span data-ttu-id="5dfce-168">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5dfce-168">OUTPUTS</span></span>

### <span data-ttu-id="5dfce-169">Microsoft.Azure.Commands.ExesDB.Models.PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="5dfce-169">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="5dfce-170">Microsoft.Azure.Commands.DiesDB.Exceptions.ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="5dfce-170">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="5dfce-171">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="5dfce-171">NOTES</span></span>

## <span data-ttu-id="5dfce-172">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="5dfce-172">RELATED LINKS</span></span>
