---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqlcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlContainer.md
ms.openlocfilehash: afdd1296b01a6798d9253b7b21d15ba66f924c34
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98307987"
---
# <span data-ttu-id="0dad2-101">New-AzCosmosDBSqlContainer</span><span class="sxs-lookup"><span data-stu-id="0dad2-101">New-AzCosmosDBSqlContainer</span></span>

## <span data-ttu-id="0dad2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0dad2-102">SYNOPSIS</span></span>
<span data-ttu-id="0dad2-103">Erstellt einen neuen Sql Container für AbensDB.</span><span class="sxs-lookup"><span data-stu-id="0dad2-103">Creates a new CosmosDB Sql Container.</span></span>

## <span data-ttu-id="0dad2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0dad2-104">SYNTAX</span></span>

### <span data-ttu-id="0dad2-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="0dad2-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBSqlContainer -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-IndexingPolicy <PSSqlIndexingPolicy>] [-PartitionKeyVersion <Int32>]
 -PartitionKeyKind <String> -PartitionKeyPath <String[]> [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>] [-UniqueKeyPolicy <PSSqlUniqueKeyPolicy>]
 [-ConflictResolutionPolicyMode <String>] [-ConflictResolutionPolicyPath <String>]
 [-ConflictResolutionPolicyProcedure <String>] [-ConflictResolutionPolicy <PSSqlConflictResolutionPolicy>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0dad2-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0dad2-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBSqlContainer -Name <String> [-IndexingPolicy <PSSqlIndexingPolicy>]
 [-PartitionKeyVersion <Int32>] -PartitionKeyKind <String> -PartitionKeyPath <String[]> [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>] [-UniqueKeyPolicy <PSSqlUniqueKeyPolicy>]
 [-ConflictResolutionPolicyMode <String>] [-ConflictResolutionPolicyPath <String>]
 [-ConflictResolutionPolicyProcedure <String>] [-ConflictResolutionPolicy <PSSqlConflictResolutionPolicy>]
 -ParentObject <PSSqlDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0dad2-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0dad2-107">DESCRIPTION</span></span>
<span data-ttu-id="0dad2-108">Erstellt einen neuen Sql Container für AbensDB.</span><span class="sxs-lookup"><span data-stu-id="0dad2-108">Creates a new CosmosDB Sql Container.</span></span>

## <span data-ttu-id="0dad2-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0dad2-109">EXAMPLES</span></span>

### <span data-ttu-id="0dad2-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0dad2-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlContainer -AccountName myAccountName -DatabaseName myDatabaseName -ResourceGroupName myRgName -Name myContainerName -PartitionKeyPath /a/b/c -PartitionKeyKind Hash

Name     : myContainerName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/sqlDatabases/myDatabaseName/contain
           ers/myContainerName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetPropertiesResource
```

## <span data-ttu-id="0dad2-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0dad2-111">PARAMETERS</span></span>

### <span data-ttu-id="0dad2-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="0dad2-112">-AccountName</span></span>
<span data-ttu-id="0dad2-113">Der Name des Dbdatenbankkontos von Db.</span><span class="sxs-lookup"><span data-stu-id="0dad2-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="0dad2-114">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="0dad2-114">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="0dad2-115">Der maximale Durchsatzwert, wenn die Automatische Skalierung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="0dad2-115">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="0dad2-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0dad2-116">-Confirm</span></span>
<span data-ttu-id="0dad2-117">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0dad2-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0dad2-118">-ConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="0dad2-118">-ConflictResolutionPolicy</span></span>
<span data-ttu-id="0dad2-119">ConflictResolutionPolicy-Objekt vom Typ PSSqlConflictResolutionPolicy, wenn dies als "ConflictResolutionPolicy" des Containers festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="0dad2-119">ConflictResolutionPolicy Object of type PSSqlConflictResolutionPolicy, when provided this is set as the ConflictResolutionPolicy of the container.</span></span>

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

### <span data-ttu-id="0dad2-120">-ConflictResolutionPolicyMode</span><span class="sxs-lookup"><span data-stu-id="0dad2-120">-ConflictResolutionPolicyMode</span></span>
<span data-ttu-id="0dad2-121">Kann die Werte haben: LastWriterWins, Custom, Manual.</span><span class="sxs-lookup"><span data-stu-id="0dad2-121">Can have the values: LastWriterWins, Custom, Manual.</span></span>
<span data-ttu-id="0dad2-122">Wenn diese Zusammen mit dem Parameter "ConflictResolutionPolicy" angegeben wird, wird sie ignoriert.</span><span class="sxs-lookup"><span data-stu-id="0dad2-122">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

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

### <span data-ttu-id="0dad2-123">-ConflictResolutionPolicyPath</span><span class="sxs-lookup"><span data-stu-id="0dad2-123">-ConflictResolutionPolicyPath</span></span>
<span data-ttu-id="0dad2-124">Wird bereitgestellt, wenn der Typ "LastWriterWins" ist.</span><span class="sxs-lookup"><span data-stu-id="0dad2-124">To be provided when the type is LastWriterWins.</span></span>
<span data-ttu-id="0dad2-125">Wenn diese Zusammen mit dem Parameter "ConflictResolutionPolicy" angegeben wird, wird sie ignoriert.</span><span class="sxs-lookup"><span data-stu-id="0dad2-125">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

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

### <span data-ttu-id="0dad2-126">-ConflictResolutionPolicyProcedure</span><span class="sxs-lookup"><span data-stu-id="0dad2-126">-ConflictResolutionPolicyProcedure</span></span>
<span data-ttu-id="0dad2-127">Wird bereitgestellt, wenn es sich um einen benutzerdefinierten Typ handelt.</span><span class="sxs-lookup"><span data-stu-id="0dad2-127">To be provided when the type is custom.</span></span>
<span data-ttu-id="0dad2-128">Wenn diese Zusammen mit dem Parameter "ConflictResolutionPolicy" angegeben wird, wird sie ignoriert.</span><span class="sxs-lookup"><span data-stu-id="0dad2-128">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

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

### <span data-ttu-id="0dad2-129">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="0dad2-129">-DatabaseName</span></span>
<span data-ttu-id="0dad2-130">Datenbankname.</span><span class="sxs-lookup"><span data-stu-id="0dad2-130">Database name.</span></span>

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

### <span data-ttu-id="0dad2-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0dad2-131">-DefaultProfile</span></span>
<span data-ttu-id="0dad2-132">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0dad2-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0dad2-133">-IndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="0dad2-133">-IndexingPolicy</span></span>
<span data-ttu-id="0dad2-134">Indizierungsrichtlinienobjekt vom Typ "Microsoft.Azure.Commands.UmsDB.PSSqlIndexingPolicy".</span><span class="sxs-lookup"><span data-stu-id="0dad2-134">Indexing Policy Object of type Microsoft.Azure.Commands.CosmosDB.PSSqlIndexingPolicy.</span></span>

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

### <span data-ttu-id="0dad2-135">-Name</span><span class="sxs-lookup"><span data-stu-id="0dad2-135">-Name</span></span>
<span data-ttu-id="0dad2-136">Containername.</span><span class="sxs-lookup"><span data-stu-id="0dad2-136">Container name.</span></span>

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

### <span data-ttu-id="0dad2-137">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="0dad2-137">-ParentObject</span></span>
<span data-ttu-id="0dad2-138">Sql-Datenbankobjekt.</span><span class="sxs-lookup"><span data-stu-id="0dad2-138">Sql Database object.</span></span>

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

### <span data-ttu-id="0dad2-139">-PartitionKeyKind</span><span class="sxs-lookup"><span data-stu-id="0dad2-139">-PartitionKeyKind</span></span>
<span data-ttu-id="0dad2-140">Die Art des Algorithmus, der für die Partitionierung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="0dad2-140">The kind of algorithm used for partitioning.</span></span>
<span data-ttu-id="0dad2-141">Mögliche Werte sind: 'Hash', 'Range'</span><span class="sxs-lookup"><span data-stu-id="0dad2-141">Possible values include: 'Hash', 'Range'</span></span>

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

### <span data-ttu-id="0dad2-142">-PartitionKeyPath</span><span class="sxs-lookup"><span data-stu-id="0dad2-142">-PartitionKeyPath</span></span>
<span data-ttu-id="0dad2-143">Partition Key Path, z. B. '/address/zipcode'.</span><span class="sxs-lookup"><span data-stu-id="0dad2-143">Partition Key Path, e.g., '/address/zipcode'.</span></span>

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

### <span data-ttu-id="0dad2-144">-PartitionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="0dad2-144">-PartitionKeyVersion</span></span>
<span data-ttu-id="0dad2-145">Die Version der Definition des Partitionsschlüssels</span><span class="sxs-lookup"><span data-stu-id="0dad2-145">The version of the partition key definition</span></span>

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

### <span data-ttu-id="0dad2-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0dad2-146">-ResourceGroupName</span></span>
<span data-ttu-id="0dad2-147">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="0dad2-147">Name of resource group.</span></span>

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

### <span data-ttu-id="0dad2-148">-Throughput</span><span class="sxs-lookup"><span data-stu-id="0dad2-148">-Throughput</span></span>
<span data-ttu-id="0dad2-149">Der Durchsatz SQL Container (RU/s).</span><span class="sxs-lookup"><span data-stu-id="0dad2-149">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="0dad2-150">Der Standardwert ist 400.</span><span class="sxs-lookup"><span data-stu-id="0dad2-150">Default value is 400.</span></span>

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

### <span data-ttu-id="0dad2-151">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="0dad2-151">-TtlInSeconds</span></span>
<span data-ttu-id="0dad2-152">Standard-Ttl in Sekunden.</span><span class="sxs-lookup"><span data-stu-id="0dad2-152">Default Ttl in seconds.</span></span>
<span data-ttu-id="0dad2-153">Wenn der Wert fehlt oder auf -1 festgelegt ist, laufen die Elemente nicht ab.</span><span class="sxs-lookup"><span data-stu-id="0dad2-153">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="0dad2-154">Wenn der Wert auf "n" festgelegt ist, laufen die Elemente n Sekunden nach der letzten Änderung ab.</span><span class="sxs-lookup"><span data-stu-id="0dad2-154">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="0dad2-155">-UniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="0dad2-155">-UniqueKeyPolicy</span></span>
<span data-ttu-id="0dad2-156">UniqueKeyPolicy-Objekt vom Typ "Microsoft.Azure.Commands.UmsDB.PSSqlUniqueKeyPolicy".</span><span class="sxs-lookup"><span data-stu-id="0dad2-156">UniqueKeyPolicy Object of type Microsoft.Azure.Commands.CosmosDB.PSSqlUniqueKeyPolicy.</span></span>

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

### <span data-ttu-id="0dad2-157">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="0dad2-157">-WhatIf</span></span>
<span data-ttu-id="0dad2-158">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0dad2-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0dad2-159">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0dad2-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0dad2-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0dad2-160">CommonParameters</span></span>
<span data-ttu-id="0dad2-161">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0dad2-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0dad2-162">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0dad2-162">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0dad2-163">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0dad2-163">INPUTS</span></span>

### <span data-ttu-id="0dad2-164">Microsoft.Azure.Commands.DiesDB.Models.PSSqlIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="0dad2-164">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlIndexingPolicy</span></span>

### <span data-ttu-id="0dad2-165">Microsoft.Azure.Commands.DiesDB.Models.PSSqlUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="0dad2-165">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKeyPolicy</span></span>

### <span data-ttu-id="0dad2-166">Microsoft.Azure.Commands.SkriptsDB.Models.PSSqlConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="0dad2-166">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlConflictResolutionPolicy</span></span>

### <span data-ttu-id="0dad2-167">Microsoft.Azure.Commands.ExesDB.Models.PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="0dad2-167">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

## <span data-ttu-id="0dad2-168">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0dad2-168">OUTPUTS</span></span>

### <span data-ttu-id="0dad2-169">Microsoft.Azure.Commands.ExesDB.Models.PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="0dad2-169">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="0dad2-170">Microsoft.Azure.Commands.DiesDB.Exceptions.ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="0dad2-170">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="0dad2-171">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="0dad2-171">NOTES</span></span>

## <span data-ttu-id="0dad2-172">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="0dad2-172">RELATED LINKS</span></span>
