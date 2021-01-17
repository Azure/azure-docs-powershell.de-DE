---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbgremlingraph
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinGraph.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinGraph.md
ms.openlocfilehash: b69640eb2af37ce0ef48ca3841c3cadcc0c3a57b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98472777"
---
# <span data-ttu-id="f1512-101">Update-AzCosmosDBGremlinGraph</span><span class="sxs-lookup"><span data-stu-id="f1512-101">Update-AzCosmosDBGremlinGraph</span></span>

## <span data-ttu-id="f1512-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f1512-102">SYNOPSIS</span></span>
<span data-ttu-id="f1512-103">Aktualisiert das GraphensDb Gremlin Graph aus Durchschmlin.</span><span class="sxs-lookup"><span data-stu-id="f1512-103">Updates the CosmosDB Gremlin Graph.</span></span> <span data-ttu-id="f1512-104">Führt einen clientseitigen Patchvorgang durch, indem das vorhandene Graph gelesen wird.</span><span class="sxs-lookup"><span data-stu-id="f1512-104">Performs a client side patch operation by reading the existing Graph.</span></span>

## <span data-ttu-id="f1512-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f1512-105">SYNTAX</span></span>

### <span data-ttu-id="f1512-106">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="f1512-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBGremlinGraph -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 [-Name <String>] [-IndexingPolicy <PSIndexingPolicy>] [-PartitionKeyVersion <Int32>]
 [-PartitionKeyKind <String>] [-PartitionKeyPath <String[]>] [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>] [-UniqueKeyPolicy <PSUniqueKeyPolicy>]
 [-ConflictResolutionPolicyMode <String>] [-ConflictResolutionPolicyPath <String>]
 [-ConflictResolutionPolicyProcedure <String>] [-ConflictResolutionPolicy <PSConflictResolutionPolicy>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1512-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f1512-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinGraph [-Name <String>] [-IndexingPolicy <PSIndexingPolicy>]
 [-PartitionKeyVersion <Int32>] [-PartitionKeyKind <String>] [-PartitionKeyPath <String[]>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-UniqueKeyPolicy <PSUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSConflictResolutionPolicy>] -ParentObject <PSGremlinDatabaseGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1512-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f1512-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinGraph [-Name <String>] [-IndexingPolicy <PSIndexingPolicy>]
 [-PartitionKeyVersion <Int32>] [-PartitionKeyKind <String>] [-PartitionKeyPath <String[]>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-UniqueKeyPolicy <PSUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSConflictResolutionPolicy>] -InputObject <PSGremlinGraphGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f1512-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f1512-109">DESCRIPTION</span></span>
<span data-ttu-id="f1512-110">Aktualisiert das GraphensDb Gremlin Graph aus Durchschmlin.</span><span class="sxs-lookup"><span data-stu-id="f1512-110">Updates the CosmosDB Gremlin Graph.</span></span> <span data-ttu-id="f1512-111">Führt einen clientseitigen Patchvorgang durch, indem das vorhandene Graph gelesen wird.</span><span class="sxs-lookup"><span data-stu-id="f1512-111">Performs a client side patch operation by reading the existing Graph.</span></span>

## <span data-ttu-id="f1512-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f1512-112">EXAMPLES</span></span>

### <span data-ttu-id="f1512-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f1512-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBGremlinGraph -AccountName myAccountName -DatabaseName myDatabaseName -ResourceGroupName myRgName -Name myContainerName -Throughput updatedThroughputValue

Name     : myContainerName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/gremlinDatabases/myDatabaseName/graphs/myGraphName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetPropertiesResource
```

## <span data-ttu-id="f1512-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f1512-114">PARAMETERS</span></span>

### <span data-ttu-id="f1512-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="f1512-115">-AccountName</span></span>
<span data-ttu-id="f1512-116">Der Name des Dbdatenbankkontos von Db.</span><span class="sxs-lookup"><span data-stu-id="f1512-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="f1512-117">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="f1512-117">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="f1512-118">Der maximale Durchsatzwert, wenn die Automatische Skalierung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="f1512-118">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="f1512-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f1512-119">-Confirm</span></span>
<span data-ttu-id="f1512-120">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f1512-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1512-121">-ConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="f1512-121">-ConflictResolutionPolicy</span></span>
<span data-ttu-id="f1512-122">ConflictResolutionPolicy-Objekt vom Typ "PSConflictResolutionPolicy", wenn dies als "ConflictResolutionPolicy" des Containers festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="f1512-122">ConflictResolutionPolicy Object of type PSConflictResolutionPolicy, when provided this is set as the ConflictResolutionPolicy of the container.</span></span>

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

### <span data-ttu-id="f1512-123">-ConflictResolutionPolicyMode</span><span class="sxs-lookup"><span data-stu-id="f1512-123">-ConflictResolutionPolicyMode</span></span>
<span data-ttu-id="f1512-124">Kann die Werte haben: LastWriterWins, Custom, Manual.</span><span class="sxs-lookup"><span data-stu-id="f1512-124">Can have the values: LastWriterWins, Custom, Manual.</span></span>

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

### <span data-ttu-id="f1512-125">-ConflictResolutionPolicyPath</span><span class="sxs-lookup"><span data-stu-id="f1512-125">-ConflictResolutionPolicyPath</span></span>
<span data-ttu-id="f1512-126">Wird bereitgestellt, wenn der Typ "LastWriterWins" ist.</span><span class="sxs-lookup"><span data-stu-id="f1512-126">To be provided when the type is LastWriterWins.</span></span>

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

### <span data-ttu-id="f1512-127">-ConflictResolutionPolicyProcedure</span><span class="sxs-lookup"><span data-stu-id="f1512-127">-ConflictResolutionPolicyProcedure</span></span>
<span data-ttu-id="f1512-128">Wird bereitgestellt, wenn es sich um einen benutzerdefinierten Typ handelt.</span><span class="sxs-lookup"><span data-stu-id="f1512-128">To be provided when the type is custom.</span></span>

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

### <span data-ttu-id="f1512-129">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f1512-129">-DatabaseName</span></span>
<span data-ttu-id="f1512-130">Datenbankname.</span><span class="sxs-lookup"><span data-stu-id="f1512-130">Database name.</span></span>

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

### <span data-ttu-id="f1512-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1512-131">-DefaultProfile</span></span>
<span data-ttu-id="f1512-132">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f1512-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f1512-133">-IndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="f1512-133">-IndexingPolicy</span></span>
<span data-ttu-id="f1512-134">Indizierungsrichtlinienobjekt vom Typ "Microsoft.Azure.Commands.UmsDB.PSIndexingPolicy".</span><span class="sxs-lookup"><span data-stu-id="f1512-134">Indexing Policy Object of type Microsoft.Azure.Commands.CosmosDB.PSIndexingPolicy.</span></span>

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

### <span data-ttu-id="f1512-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f1512-135">-InputObject</span></span>
<span data-ttu-id="f1512-136">Gremlin Graph-Objekt.</span><span class="sxs-lookup"><span data-stu-id="f1512-136">Gremlin Graph object.</span></span>

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

### <span data-ttu-id="f1512-137">-Name</span><span class="sxs-lookup"><span data-stu-id="f1512-137">-Name</span></span>
<span data-ttu-id="f1512-138">Gremlin Graph Name.</span><span class="sxs-lookup"><span data-stu-id="f1512-138">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="f1512-139">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="f1512-139">-ParentObject</span></span>
<span data-ttu-id="f1512-140">Das Gremlin-Datenbankobjekt.</span><span class="sxs-lookup"><span data-stu-id="f1512-140">Gremlin Database object.</span></span>

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

### <span data-ttu-id="f1512-141">-PartitionKeyKind</span><span class="sxs-lookup"><span data-stu-id="f1512-141">-PartitionKeyKind</span></span>
<span data-ttu-id="f1512-142">Die Art des Algorithmus, der für die Partitionierung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f1512-142">The kind of algorithm used for partitioning.</span></span>
<span data-ttu-id="f1512-143">Mögliche Werte sind: 'Hash', 'Range'</span><span class="sxs-lookup"><span data-stu-id="f1512-143">Possible values include: 'Hash', 'Range'</span></span>

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

### <span data-ttu-id="f1512-144">-PartitionKeyPath</span><span class="sxs-lookup"><span data-stu-id="f1512-144">-PartitionKeyPath</span></span>
<span data-ttu-id="f1512-145">Partition Key Path, z. B. '/address/zipcode'.</span><span class="sxs-lookup"><span data-stu-id="f1512-145">Partition Key Path, e.g., '/address/zipcode'.</span></span>

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

### <span data-ttu-id="f1512-146">-PartitionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="f1512-146">-PartitionKeyVersion</span></span>
<span data-ttu-id="f1512-147">Die Version der Definition des Partitionsschlüssels</span><span class="sxs-lookup"><span data-stu-id="f1512-147">The version of the partition key definition</span></span>

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

### <span data-ttu-id="f1512-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1512-148">-ResourceGroupName</span></span>
<span data-ttu-id="f1512-149">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="f1512-149">Name of resource group.</span></span>

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

### <span data-ttu-id="f1512-150">-Throughput</span><span class="sxs-lookup"><span data-stu-id="f1512-150">-Throughput</span></span>
<span data-ttu-id="f1512-151">Der Durchsatz von Gremlin Graph (RU/s).</span><span class="sxs-lookup"><span data-stu-id="f1512-151">The throughput of Gremlin Graph (RU/s).</span></span>
<span data-ttu-id="f1512-152">Der Standardwert ist 400.</span><span class="sxs-lookup"><span data-stu-id="f1512-152">Default value is 400.</span></span>

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

### <span data-ttu-id="f1512-153">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="f1512-153">-TtlInSeconds</span></span>
<span data-ttu-id="f1512-154">Standard-Ttl in Sekunden.</span><span class="sxs-lookup"><span data-stu-id="f1512-154">Default Ttl in seconds.</span></span>
<span data-ttu-id="f1512-155">Wenn der Wert fehlt oder auf -1 festgelegt ist, laufen die Elemente nicht ab.</span><span class="sxs-lookup"><span data-stu-id="f1512-155">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="f1512-156">Wenn der Wert auf "n" festgelegt ist, laufen die Elemente n Sekunden nach der letzten Änderung ab.</span><span class="sxs-lookup"><span data-stu-id="f1512-156">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="f1512-157">-UniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="f1512-157">-UniqueKeyPolicy</span></span>
<span data-ttu-id="f1512-158">EindeutigesKeyPolicy-Objekt vom Typ "Microsoft.Azure.Commands.UmsDB.PSUniqueKeyPolicy".</span><span class="sxs-lookup"><span data-stu-id="f1512-158">UniqueKeyPolicy Object of type Microsoft.Azure.Commands.CosmosDB.PSUniqueKeyPolicy.</span></span>

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

### <span data-ttu-id="f1512-159">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="f1512-159">-WhatIf</span></span>
<span data-ttu-id="f1512-160">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f1512-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f1512-161">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f1512-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1512-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1512-162">CommonParameters</span></span>
<span data-ttu-id="f1512-163">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1512-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1512-164">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f1512-164">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1512-165">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f1512-165">INPUTS</span></span>

### <span data-ttu-id="f1512-166">Microsoft.Azure.Commands.UmsDB.Models.PSIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="f1512-166">Microsoft.Azure.Commands.CosmosDB.Models.PSIndexingPolicy</span></span>

### <span data-ttu-id="f1512-167">Microsoft.Azure.Commands.UmsDB.Models.PSUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="f1512-167">Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKeyPolicy</span></span>

### <span data-ttu-id="f1512-168">Microsoft.Azure.Commands.Durchsdb.Models.PSConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="f1512-168">Microsoft.Azure.Commands.CosmosDB.Models.PSConflictResolutionPolicy</span></span>

### <span data-ttu-id="f1512-169">Microsoft.Azure.Commands.ExesDB.Models.PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="f1512-169">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

### <span data-ttu-id="f1512-170">Microsoft.Azure.Commands.DiesDB.Models.PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="f1512-170">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

## <span data-ttu-id="f1512-171">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f1512-171">OUTPUTS</span></span>

### <span data-ttu-id="f1512-172">Microsoft.Azure.Commands.DiesDB.Models.PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="f1512-172">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

### <span data-ttu-id="f1512-173">Microsoft.Azure.Commands.Abt. Exceptions.ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="f1512-173">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="f1512-174">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="f1512-174">NOTES</span></span>

## <span data-ttu-id="f1512-175">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="f1512-175">RELATED LINKS</span></span>
