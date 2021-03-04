---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbgremlingraph
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinGraph.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinGraph.md
ms.openlocfilehash: 464dbb54a96f7f543607cd2f053a0e7360eba344
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101949451"
---
# <span data-ttu-id="d4c11-101">New-AzCosmosDBGremlinGraph</span><span class="sxs-lookup"><span data-stu-id="d4c11-101">New-AzCosmosDBGremlinGraph</span></span>

## <span data-ttu-id="d4c11-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d4c11-102">SYNOPSIS</span></span>
<span data-ttu-id="d4c11-103">Erstellt ein neues CosmosDB Gremlin Graph.</span><span class="sxs-lookup"><span data-stu-id="d4c11-103">Creates a new CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="d4c11-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d4c11-104">SYNTAX</span></span>

### <span data-ttu-id="d4c11-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="d4c11-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBGremlinGraph -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-IndexingPolicy <PSIndexingPolicy>] [-PartitionKeyVersion <Int32>] -PartitionKeyKind <String>
 -PartitionKeyPath <String[]> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-UniqueKeyPolicy <PSUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSConflictResolutionPolicy>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4c11-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d4c11-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBGremlinGraph -Name <String> [-IndexingPolicy <PSIndexingPolicy>] [-PartitionKeyVersion <Int32>]
 -PartitionKeyKind <String> -PartitionKeyPath <String[]> [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>] [-UniqueKeyPolicy <PSUniqueKeyPolicy>]
 [-ConflictResolutionPolicyMode <String>] [-ConflictResolutionPolicyPath <String>]
 [-ConflictResolutionPolicyProcedure <String>] [-ConflictResolutionPolicy <PSConflictResolutionPolicy>]
 -ParentObject <PSGremlinDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d4c11-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d4c11-107">DESCRIPTION</span></span>
<span data-ttu-id="d4c11-108">Erstellt ein neues CosmosDB Gremlin Graph.</span><span class="sxs-lookup"><span data-stu-id="d4c11-108">Creates a new CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="d4c11-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d4c11-109">EXAMPLES</span></span>

### <span data-ttu-id="d4c11-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d4c11-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBGremlinGraph -AccountName myAccountName -DatabaseName myDatabaseName -ResourceGroupName myRgName -Name myContainerName -PartitionKeyPath /a -PartitionKeyKind Hash

Name     : myContainerName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/gremlinDatabases/myDatabaseName/graphs/myGraphName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetPropertiesResource
```

## <span data-ttu-id="d4c11-111">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="d4c11-111">PARAMETERS</span></span>

### <span data-ttu-id="d4c11-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="d4c11-112">-AccountName</span></span>
<span data-ttu-id="d4c11-113">Name des Datenbankkontos "Cosmos DB".</span><span class="sxs-lookup"><span data-stu-id="d4c11-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="d4c11-114">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="d4c11-114">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="d4c11-115">Maximaler Durchsatzwert, wenn die automatische Skalierung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="d4c11-115">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="d4c11-116">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d4c11-116">-Confirm</span></span>
<span data-ttu-id="d4c11-117">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d4c11-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4c11-118">-ConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="d4c11-118">-ConflictResolutionPolicy</span></span>
<span data-ttu-id="d4c11-119">ConflictResolutionPolicy-Objekt vom Typ PSConflictResolutionPolicy, sofern dies als ConflictResolutionPolicy des Containers festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="d4c11-119">ConflictResolutionPolicy Object of type PSConflictResolutionPolicy, when provided this is set as the ConflictResolutionPolicy of the container.</span></span>

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

### <span data-ttu-id="d4c11-120">-ConflictResolutionPolicyMode</span><span class="sxs-lookup"><span data-stu-id="d4c11-120">-ConflictResolutionPolicyMode</span></span>
<span data-ttu-id="d4c11-121">Kann die Werte haben: LastWriterWins, Custom, Manual.</span><span class="sxs-lookup"><span data-stu-id="d4c11-121">Can have the values: LastWriterWins, Custom, Manual.</span></span>

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

### <span data-ttu-id="d4c11-122">-ConflictResolutionPolicyPath</span><span class="sxs-lookup"><span data-stu-id="d4c11-122">-ConflictResolutionPolicyPath</span></span>
<span data-ttu-id="d4c11-123">Wird bereitgestellt, wenn der Typ LastWriterWins ist.</span><span class="sxs-lookup"><span data-stu-id="d4c11-123">To be provided when the type is LastWriterWins.</span></span>

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

### <span data-ttu-id="d4c11-124">-ConflictResolutionPolicyProcedure</span><span class="sxs-lookup"><span data-stu-id="d4c11-124">-ConflictResolutionPolicyProcedure</span></span>
<span data-ttu-id="d4c11-125">Soll bereitgestellt werden, wenn der Typ benutzerdefinierter ist.</span><span class="sxs-lookup"><span data-stu-id="d4c11-125">To be provided when the type is custom.</span></span>

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

### <span data-ttu-id="d4c11-126">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d4c11-126">-DatabaseName</span></span>
<span data-ttu-id="d4c11-127">Datenbankname.</span><span class="sxs-lookup"><span data-stu-id="d4c11-127">Database name.</span></span>

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

### <span data-ttu-id="d4c11-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4c11-128">-DefaultProfile</span></span>
<span data-ttu-id="d4c11-129">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d4c11-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d4c11-130">-IndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="d4c11-130">-IndexingPolicy</span></span>
<span data-ttu-id="d4c11-131">Indizierungsrichtlinienobjekt vom Typ Microsoft.Azure.Commands.CosmosDB.PSIndexingPolicy.</span><span class="sxs-lookup"><span data-stu-id="d4c11-131">Indexing Policy Object of type Microsoft.Azure.Commands.CosmosDB.PSIndexingPolicy.</span></span>

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

### <span data-ttu-id="d4c11-132">-Name</span><span class="sxs-lookup"><span data-stu-id="d4c11-132">-Name</span></span>
<span data-ttu-id="d4c11-133">Gremlin Graph Name.</span><span class="sxs-lookup"><span data-stu-id="d4c11-133">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="d4c11-134">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="d4c11-134">-ParentObject</span></span>
<span data-ttu-id="d4c11-135">Gremlin-Datenbankobjekt.</span><span class="sxs-lookup"><span data-stu-id="d4c11-135">Gremlin Database object.</span></span>

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

### <span data-ttu-id="d4c11-136">-PartitionKeyKind</span><span class="sxs-lookup"><span data-stu-id="d4c11-136">-PartitionKeyKind</span></span>
<span data-ttu-id="d4c11-137">Die Art des Algorithmus, der für die Partitionierung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d4c11-137">The kind of algorithm used for partitioning.</span></span>
<span data-ttu-id="d4c11-138">Mögliche Werte sind: "Hash", "Bereich"</span><span class="sxs-lookup"><span data-stu-id="d4c11-138">Possible values include: 'Hash', 'Range'</span></span>

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

### <span data-ttu-id="d4c11-139">-PartitionKeyPath</span><span class="sxs-lookup"><span data-stu-id="d4c11-139">-PartitionKeyPath</span></span>
<span data-ttu-id="d4c11-140">Partition Key Path, z. B. "/address/zipcode".</span><span class="sxs-lookup"><span data-stu-id="d4c11-140">Partition Key Path, e.g., '/address/zipcode'.</span></span>

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

### <span data-ttu-id="d4c11-141">-PartitionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="d4c11-141">-PartitionKeyVersion</span></span>
<span data-ttu-id="d4c11-142">Die Version der Partitionsschlüsseldefinition</span><span class="sxs-lookup"><span data-stu-id="d4c11-142">The version of the partition key definition</span></span>

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

### <span data-ttu-id="d4c11-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4c11-143">-ResourceGroupName</span></span>
<span data-ttu-id="d4c11-144">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="d4c11-144">Name of resource group.</span></span>

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

### <span data-ttu-id="d4c11-145">-Durchsatz</span><span class="sxs-lookup"><span data-stu-id="d4c11-145">-Throughput</span></span>
<span data-ttu-id="d4c11-146">Der Durchsatz von Gremlin Graph (RU/s).</span><span class="sxs-lookup"><span data-stu-id="d4c11-146">The throughput of Gremlin Graph (RU/s).</span></span>
<span data-ttu-id="d4c11-147">Der Standardwert ist 400.</span><span class="sxs-lookup"><span data-stu-id="d4c11-147">Default value is 400.</span></span>

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

### <span data-ttu-id="d4c11-148">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="d4c11-148">-TtlInSeconds</span></span>
<span data-ttu-id="d4c11-149">Standard-Ttl in Sekunden.</span><span class="sxs-lookup"><span data-stu-id="d4c11-149">Default Ttl in seconds.</span></span>
<span data-ttu-id="d4c11-150">Wenn der Wert fehlt oder auf - 1 festgelegt ist, laufen die Elemente nicht ab.</span><span class="sxs-lookup"><span data-stu-id="d4c11-150">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="d4c11-151">Wenn der Wert auf n festgelegt ist, laufen Elemente n Sekunden nach der letzten Änderungszeit ab.</span><span class="sxs-lookup"><span data-stu-id="d4c11-151">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="d4c11-152">-UniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="d4c11-152">-UniqueKeyPolicy</span></span>
<span data-ttu-id="d4c11-153">UniqueKeyPolicy-Objekt vom Typ Microsoft.Azure.Commands.CosmosDB.PSUniqueKeyPolicy.</span><span class="sxs-lookup"><span data-stu-id="d4c11-153">UniqueKeyPolicy Object of type Microsoft.Azure.Commands.CosmosDB.PSUniqueKeyPolicy.</span></span>

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

### <span data-ttu-id="d4c11-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4c11-154">-WhatIf</span></span>
<span data-ttu-id="d4c11-155">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d4c11-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d4c11-156">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d4c11-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d4c11-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4c11-157">CommonParameters</span></span>
<span data-ttu-id="d4c11-158">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4c11-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4c11-159">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d4c11-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4c11-160">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d4c11-160">INPUTS</span></span>

### <span data-ttu-id="d4c11-161">Microsoft.Azure.Commands.CosmosDB.Models.PSIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="d4c11-161">Microsoft.Azure.Commands.CosmosDB.Models.PSIndexingPolicy</span></span>

### <span data-ttu-id="d4c11-162">Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="d4c11-162">Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKeyPolicy</span></span>

### <span data-ttu-id="d4c11-163">Microsoft.Azure.Commands.CosmosDB.Models.PSConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="d4c11-163">Microsoft.Azure.Commands.CosmosDB.Models.PSConflictResolutionPolicy</span></span>

### <span data-ttu-id="d4c11-164">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="d4c11-164">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="d4c11-165">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d4c11-165">OUTPUTS</span></span>

### <span data-ttu-id="d4c11-166">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="d4c11-166">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

### <span data-ttu-id="d4c11-167">System.Exception</span><span class="sxs-lookup"><span data-stu-id="d4c11-167">System.Exception</span></span>

## <span data-ttu-id="d4c11-168">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="d4c11-168">NOTES</span></span>

## <span data-ttu-id="d4c11-169">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="d4c11-169">RELATED LINKS</span></span>
