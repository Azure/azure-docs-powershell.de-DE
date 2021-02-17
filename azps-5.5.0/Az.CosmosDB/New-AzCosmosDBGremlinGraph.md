---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlingraph
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinGraph.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinGraph.md
ms.openlocfilehash: ab81c97048c64a08ab29877becfd44b690312a27
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100164060"
---
# <span data-ttu-id="40b9e-101">New-AzCosmosDBGremlinGraph</span><span class="sxs-lookup"><span data-stu-id="40b9e-101">New-AzCosmosDBGremlinGraph</span></span>

## <span data-ttu-id="40b9e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="40b9e-102">SYNOPSIS</span></span>
<span data-ttu-id="40b9e-103">Erstellt ein neues Grafisches Untermain.</span><span class="sxs-lookup"><span data-stu-id="40b9e-103">Creates a new CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="40b9e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="40b9e-104">SYNTAX</span></span>

### <span data-ttu-id="40b9e-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="40b9e-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBGremlinGraph -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-IndexingPolicy <PSIndexingPolicy>] [-PartitionKeyVersion <Int32>] -PartitionKeyKind <String>
 -PartitionKeyPath <String[]> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-UniqueKeyPolicy <PSUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSConflictResolutionPolicy>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="40b9e-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="40b9e-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBGremlinGraph -Name <String> [-IndexingPolicy <PSIndexingPolicy>] [-PartitionKeyVersion <Int32>]
 -PartitionKeyKind <String> -PartitionKeyPath <String[]> [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>] [-UniqueKeyPolicy <PSUniqueKeyPolicy>]
 [-ConflictResolutionPolicyMode <String>] [-ConflictResolutionPolicyPath <String>]
 [-ConflictResolutionPolicyProcedure <String>] [-ConflictResolutionPolicy <PSConflictResolutionPolicy>]
 -ParentObject <PSGremlinDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="40b9e-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="40b9e-107">DESCRIPTION</span></span>
<span data-ttu-id="40b9e-108">Erstellt ein neues Grafisches Untermain.</span><span class="sxs-lookup"><span data-stu-id="40b9e-108">Creates a new CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="40b9e-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="40b9e-109">EXAMPLES</span></span>

### <span data-ttu-id="40b9e-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="40b9e-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBGremlinGraph -AccountName myAccountName -DatabaseName myDatabaseName -ResourceGroupName myRgName -Name myContainerName -PartitionKeyPath /a -PartitionKeyKind Hash

Name     : myContainerName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/gremlinDatabases/myDatabaseName/graphs/myGraphName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetPropertiesResource
```

## <span data-ttu-id="40b9e-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="40b9e-111">PARAMETERS</span></span>

### <span data-ttu-id="40b9e-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="40b9e-112">-AccountName</span></span>
<span data-ttu-id="40b9e-113">Der Name des Dbdatenbankkontos von Db.</span><span class="sxs-lookup"><span data-stu-id="40b9e-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="40b9e-114">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="40b9e-114">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="40b9e-115">Der maximale Durchsatzwert, wenn die Automatische Skalierung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="40b9e-115">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="40b9e-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="40b9e-116">-Confirm</span></span>
<span data-ttu-id="40b9e-117">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="40b9e-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="40b9e-118">-ConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="40b9e-118">-ConflictResolutionPolicy</span></span>
<span data-ttu-id="40b9e-119">ConflictResolutionPolicy-Objekt vom Typ "PSConflictResolutionPolicy", wenn dies als "ConflictResolutionPolicy" des Containers festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="40b9e-119">ConflictResolutionPolicy Object of type PSConflictResolutionPolicy, when provided this is set as the ConflictResolutionPolicy of the container.</span></span>

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

### <span data-ttu-id="40b9e-120">-ConflictResolutionPolicyMode</span><span class="sxs-lookup"><span data-stu-id="40b9e-120">-ConflictResolutionPolicyMode</span></span>
<span data-ttu-id="40b9e-121">Kann die Werte haben: LastWriterWins, Custom, Manual.</span><span class="sxs-lookup"><span data-stu-id="40b9e-121">Can have the values: LastWriterWins, Custom, Manual.</span></span>

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

### <span data-ttu-id="40b9e-122">-ConflictResolutionPolicyPath</span><span class="sxs-lookup"><span data-stu-id="40b9e-122">-ConflictResolutionPolicyPath</span></span>
<span data-ttu-id="40b9e-123">Wird bereitgestellt, wenn der Typ "LastWriterWins" ist.</span><span class="sxs-lookup"><span data-stu-id="40b9e-123">To be provided when the type is LastWriterWins.</span></span>

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

### <span data-ttu-id="40b9e-124">-ConflictResolutionPolicyProcedure</span><span class="sxs-lookup"><span data-stu-id="40b9e-124">-ConflictResolutionPolicyProcedure</span></span>
<span data-ttu-id="40b9e-125">Wird bereitgestellt, wenn es sich um einen benutzerdefinierten Typ handelt.</span><span class="sxs-lookup"><span data-stu-id="40b9e-125">To be provided when the type is custom.</span></span>

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

### <span data-ttu-id="40b9e-126">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="40b9e-126">-DatabaseName</span></span>
<span data-ttu-id="40b9e-127">Datenbankname.</span><span class="sxs-lookup"><span data-stu-id="40b9e-127">Database name.</span></span>

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

### <span data-ttu-id="40b9e-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40b9e-128">-DefaultProfile</span></span>
<span data-ttu-id="40b9e-129">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="40b9e-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="40b9e-130">-IndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="40b9e-130">-IndexingPolicy</span></span>
<span data-ttu-id="40b9e-131">Indizierungsrichtlinienobjekt vom Typ "Microsoft.Azure.Commands.UmsDB.PSIndexingPolicy".</span><span class="sxs-lookup"><span data-stu-id="40b9e-131">Indexing Policy Object of type Microsoft.Azure.Commands.CosmosDB.PSIndexingPolicy.</span></span>

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

### <span data-ttu-id="40b9e-132">-Name</span><span class="sxs-lookup"><span data-stu-id="40b9e-132">-Name</span></span>
<span data-ttu-id="40b9e-133">Name von Gremlin Graph.</span><span class="sxs-lookup"><span data-stu-id="40b9e-133">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="40b9e-134">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="40b9e-134">-ParentObject</span></span>
<span data-ttu-id="40b9e-135">Das Objekt "Gremlin-Datenbank".</span><span class="sxs-lookup"><span data-stu-id="40b9e-135">Gremlin Database object.</span></span>

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

### <span data-ttu-id="40b9e-136">-PartitionKeyKind</span><span class="sxs-lookup"><span data-stu-id="40b9e-136">-PartitionKeyKind</span></span>
<span data-ttu-id="40b9e-137">Die Art des Algorithmus, der für die Partitionierung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="40b9e-137">The kind of algorithm used for partitioning.</span></span>
<span data-ttu-id="40b9e-138">Mögliche Werte sind: 'Hash', 'Range'</span><span class="sxs-lookup"><span data-stu-id="40b9e-138">Possible values include: 'Hash', 'Range'</span></span>

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

### <span data-ttu-id="40b9e-139">-PartitionKeyPath</span><span class="sxs-lookup"><span data-stu-id="40b9e-139">-PartitionKeyPath</span></span>
<span data-ttu-id="40b9e-140">Partition Key Path, z. B. '/address/zipcode'.</span><span class="sxs-lookup"><span data-stu-id="40b9e-140">Partition Key Path, e.g., '/address/zipcode'.</span></span>

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

### <span data-ttu-id="40b9e-141">-PartitionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="40b9e-141">-PartitionKeyVersion</span></span>
<span data-ttu-id="40b9e-142">Die Version der Definition des Partitionsschlüssels</span><span class="sxs-lookup"><span data-stu-id="40b9e-142">The version of the partition key definition</span></span>

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

### <span data-ttu-id="40b9e-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40b9e-143">-ResourceGroupName</span></span>
<span data-ttu-id="40b9e-144">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="40b9e-144">Name of resource group.</span></span>

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

### <span data-ttu-id="40b9e-145">-Throughput</span><span class="sxs-lookup"><span data-stu-id="40b9e-145">-Throughput</span></span>
<span data-ttu-id="40b9e-146">Der Durchsatz von Gremlin Graph (RU/s).</span><span class="sxs-lookup"><span data-stu-id="40b9e-146">The throughput of Gremlin Graph (RU/s).</span></span>
<span data-ttu-id="40b9e-147">Der Standardwert ist 400.</span><span class="sxs-lookup"><span data-stu-id="40b9e-147">Default value is 400.</span></span>

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

### <span data-ttu-id="40b9e-148">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="40b9e-148">-TtlInSeconds</span></span>
<span data-ttu-id="40b9e-149">Standard-Ttl in Sekunden.</span><span class="sxs-lookup"><span data-stu-id="40b9e-149">Default Ttl in seconds.</span></span>
<span data-ttu-id="40b9e-150">Wenn der Wert fehlt oder auf -1 festgelegt ist, laufen die Elemente nicht ab.</span><span class="sxs-lookup"><span data-stu-id="40b9e-150">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="40b9e-151">Wenn der Wert auf "n" festgelegt ist, laufen die Elemente n Sekunden nach der letzten Änderung ab.</span><span class="sxs-lookup"><span data-stu-id="40b9e-151">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="40b9e-152">-UniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="40b9e-152">-UniqueKeyPolicy</span></span>
<span data-ttu-id="40b9e-153">EindeutigesKeyPolicy-Objekt vom Typ "Microsoft.Azure.Commands.UmsDB.PSUniqueKeyPolicy".</span><span class="sxs-lookup"><span data-stu-id="40b9e-153">UniqueKeyPolicy Object of type Microsoft.Azure.Commands.CosmosDB.PSUniqueKeyPolicy.</span></span>

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

### <span data-ttu-id="40b9e-154">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="40b9e-154">-WhatIf</span></span>
<span data-ttu-id="40b9e-155">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="40b9e-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="40b9e-156">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="40b9e-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="40b9e-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40b9e-157">CommonParameters</span></span>
<span data-ttu-id="40b9e-158">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40b9e-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40b9e-159">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="40b9e-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40b9e-160">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="40b9e-160">INPUTS</span></span>

### <span data-ttu-id="40b9e-161">Microsoft.Azure.Commands.DiesDB.Models.PSIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="40b9e-161">Microsoft.Azure.Commands.CosmosDB.Models.PSIndexingPolicy</span></span>

### <span data-ttu-id="40b9e-162">Microsoft.Azure.Commands.DiesDB.Models.PSUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="40b9e-162">Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKeyPolicy</span></span>

### <span data-ttu-id="40b9e-163">Microsoft.Azure.Commands.DiesDB.Models.PSConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="40b9e-163">Microsoft.Azure.Commands.CosmosDB.Models.PSConflictResolutionPolicy</span></span>

### <span data-ttu-id="40b9e-164">Microsoft.Azure.Commands.ExesDB.Models.PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="40b9e-164">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="40b9e-165">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="40b9e-165">OUTPUTS</span></span>

### <span data-ttu-id="40b9e-166">Microsoft.Azure.Commands.ExesDB.Models.PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="40b9e-166">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

### <span data-ttu-id="40b9e-167">System.Exception</span><span class="sxs-lookup"><span data-stu-id="40b9e-167">System.Exception</span></span>

## <span data-ttu-id="40b9e-168">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="40b9e-168">NOTES</span></span>

## <span data-ttu-id="40b9e-169">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="40b9e-169">RELATED LINKS</span></span>
