---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/set-azcosmosdbgremlingraph
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBGremlinGraph.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBGremlinGraph.md
ms.openlocfilehash: a8ccb3757786ca76fff15b1bf68d8dc7b477ebcc
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94004644"
---
# <span data-ttu-id="b9fae-101">Set-AzCosmosDBGremlinGraph</span><span class="sxs-lookup"><span data-stu-id="b9fae-101">Set-AzCosmosDBGremlinGraph</span></span>

## <span data-ttu-id="b9fae-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b9fae-102">SYNOPSIS</span></span>
<span data-ttu-id="b9fae-103">Legt das CosmosDB-Gremlin-Diagramm fest.</span><span class="sxs-lookup"><span data-stu-id="b9fae-103">Sets the CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="b9fae-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b9fae-104">SYNTAX</span></span>

### <span data-ttu-id="b9fae-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="b9fae-105">ByNameParameterSet (Default)</span></span>
```
Set-AzCosmosDBGremlinGraph -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-IndexingPolicy <PSIndexingPolicy>] [-PartitionKeyVersion <Int32>] -PartitionKeyKind <String>
 -PartitionKeyPath <String[]> [-Throughput <Int32>] [-TtlInSeconds <Int32>]
 [-UniqueKeyPolicy <PSUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSConflictResolutionPolicy>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b9fae-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b9fae-106">ByParentObjectParameterSet</span></span>
```
Set-AzCosmosDBGremlinGraph -Name <String> [-IndexingPolicy <PSIndexingPolicy>] [-PartitionKeyVersion <Int32>]
 -PartitionKeyKind <String> -PartitionKeyPath <String[]> [-Throughput <Int32>] [-TtlInSeconds <Int32>]
 [-UniqueKeyPolicy <PSUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSConflictResolutionPolicy>] -InputObject <PSGremlinDatabaseGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b9fae-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b9fae-107">DESCRIPTION</span></span>
<span data-ttu-id="b9fae-108">Das Cmdlet " **Set-AzCosmosDBGremlinGraph** " legt ein CosmosDB-Gremlin-Diagramm fest.</span><span class="sxs-lookup"><span data-stu-id="b9fae-108">The **Set-AzCosmosDBGremlinGraph** cmdlet sets a CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="b9fae-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b9fae-109">EXAMPLES</span></span>

### <span data-ttu-id="b9fae-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b9fae-110">Example 1</span></span>
```powershell
PS C:\> Set-AzCosmosDBGremlinGraph -ResourceGroupName {rgName} -AccountName {accountName} -DatabaseName {dbName} -Name {graphName} -PartitionKeyPath {path}

Name        Id    Resource
----        --    -------
{name}     {id}   Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetPropertiesResource
```

<span data-ttu-id="b9fae-111">Das Ressourcenobjekt enthält IndexingPolicy, PartitionKey, DefaultTtl, UniqueKeyPolicy, ConflictResolutionPolicy, _rid, _ts, _etag.</span><span class="sxs-lookup"><span data-stu-id="b9fae-111">Resource Object contains IndexingPolicy, PartitionKey, DefaultTtl, UniqueKeyPolicy, ConflictResolutionPolicy, _rid, _ts, _etag.</span></span>

## <span data-ttu-id="b9fae-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="b9fae-112">PARAMETERS</span></span>

### <span data-ttu-id="b9fae-113">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="b9fae-113">-AccountName</span></span>
<span data-ttu-id="b9fae-114">Name des Cosmos DB-Daten Bankkontos.</span><span class="sxs-lookup"><span data-stu-id="b9fae-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="b9fae-115">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b9fae-115">-Confirm</span></span>
<span data-ttu-id="b9fae-116">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b9fae-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b9fae-117">-ConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="b9fae-117">-ConflictResolutionPolicy</span></span>
<span data-ttu-id="b9fae-118">ConflictResolutionPolicy-Objekt vom Typ PSConflictResolutionPolicy, wenn diese Einstellung als ConflictResolutionPolicy des Containers angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="b9fae-118">ConflictResolutionPolicy Object of type PSConflictResolutionPolicy, when provided this is set as the ConflictResolutionPolicy of the container.</span></span>

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

### <span data-ttu-id="b9fae-119">-ConflictResolutionPolicyMode</span><span class="sxs-lookup"><span data-stu-id="b9fae-119">-ConflictResolutionPolicyMode</span></span>
<span data-ttu-id="b9fae-120">Kann die Werte haben: LastWriterWins, Benutzerdefiniert, manuell.</span><span class="sxs-lookup"><span data-stu-id="b9fae-120">Can have the values: LastWriterWins, Custom, Manual.</span></span>

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

### <span data-ttu-id="b9fae-121">-ConflictResolutionPolicyPath</span><span class="sxs-lookup"><span data-stu-id="b9fae-121">-ConflictResolutionPolicyPath</span></span>
<span data-ttu-id="b9fae-122">, Die bereitgestellt werden soll, wenn der Typ LastWriterWins ist.</span><span class="sxs-lookup"><span data-stu-id="b9fae-122">To be provided when the type is LastWriterWins.</span></span>

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

### <span data-ttu-id="b9fae-123">-ConflictResolutionPolicyProcedure</span><span class="sxs-lookup"><span data-stu-id="b9fae-123">-ConflictResolutionPolicyProcedure</span></span>
<span data-ttu-id="b9fae-124">, Die bereitgestellt werden soll, wenn der Typ Benutzerdefiniert ist.</span><span class="sxs-lookup"><span data-stu-id="b9fae-124">To be provided when the type is custom.</span></span>

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

### <span data-ttu-id="b9fae-125">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b9fae-125">-DatabaseName</span></span>
<span data-ttu-id="b9fae-126">Datenbankname</span><span class="sxs-lookup"><span data-stu-id="b9fae-126">Database name.</span></span>

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

### <span data-ttu-id="b9fae-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9fae-127">-DefaultProfile</span></span>
<span data-ttu-id="b9fae-128">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b9fae-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b9fae-129">-IndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="b9fae-129">-IndexingPolicy</span></span>
<span data-ttu-id="b9fae-130">Indizierungs Richtlinienobjekt vom Typ Microsoft. Azure. Commands. CosmosDB. PSSqlIndexingPolicy.</span><span class="sxs-lookup"><span data-stu-id="b9fae-130">Indexing Policy Object of type Microsoft.Azure.Commands.CosmosDB.PSSqlIndexingPolicy.</span></span>

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

### <span data-ttu-id="b9fae-131">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="b9fae-131">-InputObject</span></span>
<span data-ttu-id="b9fae-132">Gremlin-Datenbankobjekt.</span><span class="sxs-lookup"><span data-stu-id="b9fae-132">Gremlin Database object.</span></span>

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

### <span data-ttu-id="b9fae-133">-Name</span><span class="sxs-lookup"><span data-stu-id="b9fae-133">-Name</span></span>
<span data-ttu-id="b9fae-134">Gremlin-Diagramm Name</span><span class="sxs-lookup"><span data-stu-id="b9fae-134">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="b9fae-135">-PartitionKeyKind</span><span class="sxs-lookup"><span data-stu-id="b9fae-135">-PartitionKeyKind</span></span>
<span data-ttu-id="b9fae-136">Die Art des für die Partitionierung verwendeten Algorithmus.</span><span class="sxs-lookup"><span data-stu-id="b9fae-136">The kind of algorithm used for partitioning.</span></span>
<span data-ttu-id="b9fae-137">Mögliche Werte sind: "Hash"; "Bereich"</span><span class="sxs-lookup"><span data-stu-id="b9fae-137">Possible values include: 'Hash', 'Range'</span></span>

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

### <span data-ttu-id="b9fae-138">-PartitionKeyPath</span><span class="sxs-lookup"><span data-stu-id="b9fae-138">-PartitionKeyPath</span></span>
<span data-ttu-id="b9fae-139">Partitionsschlüssel Pfad, beispielsweise "/Address/ZipCode".</span><span class="sxs-lookup"><span data-stu-id="b9fae-139">Partition Key Path, e.g., '/address/zipcode'.</span></span>

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

### <span data-ttu-id="b9fae-140">-PartitionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="b9fae-140">-PartitionKeyVersion</span></span>
<span data-ttu-id="b9fae-141">Die Version der Partitionsschlüssel Definition</span><span class="sxs-lookup"><span data-stu-id="b9fae-141">The version of the partition key definition</span></span>

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

### <span data-ttu-id="b9fae-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9fae-142">-ResourceGroupName</span></span>
<span data-ttu-id="b9fae-143">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="b9fae-143">Name of resource group.</span></span>

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

### <span data-ttu-id="b9fae-144">-Durchsatz</span><span class="sxs-lookup"><span data-stu-id="b9fae-144">-Throughput</span></span>
<span data-ttu-id="b9fae-145">Der Durchsatz von Gremlin Graph (ru/s).</span><span class="sxs-lookup"><span data-stu-id="b9fae-145">The throughput of Gremlin Graph (RU/s).</span></span>
<span data-ttu-id="b9fae-146">Der Standardwert ist 400.</span><span class="sxs-lookup"><span data-stu-id="b9fae-146">Default value is 400.</span></span>

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

### <span data-ttu-id="b9fae-147">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="b9fae-147">-TtlInSeconds</span></span>
<span data-ttu-id="b9fae-148">Standard-TTL in Sekunden.</span><span class="sxs-lookup"><span data-stu-id="b9fae-148">Default Ttl in seconds.</span></span>
<span data-ttu-id="b9fae-149">Wenn der Wert fehlt oder auf-1 gesetzt ist, werden die Elemente nicht ablaufen.</span><span class="sxs-lookup"><span data-stu-id="b9fae-149">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="b9fae-150">Wenn der Wert auf n gesetzt ist, werden die Elemente nach dem Zeitpunkt der letzten Änderung n Sekunden ablaufen.</span><span class="sxs-lookup"><span data-stu-id="b9fae-150">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="b9fae-151">-UniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="b9fae-151">-UniqueKeyPolicy</span></span>
<span data-ttu-id="b9fae-152">UniqueKeyPolicy-Objekt vom Typ Microsoft. Azure. Commands. CosmosDB. PSSqlUniqueKeyPolicy.</span><span class="sxs-lookup"><span data-stu-id="b9fae-152">UniqueKeyPolicy Object of type Microsoft.Azure.Commands.CosmosDB.PSSqlUniqueKeyPolicy.</span></span>

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

### <span data-ttu-id="b9fae-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9fae-153">-WhatIf</span></span>
<span data-ttu-id="b9fae-154">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b9fae-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b9fae-155">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b9fae-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b9fae-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9fae-156">CommonParameters</span></span>
<span data-ttu-id="b9fae-157">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9fae-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9fae-158">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b9fae-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9fae-159">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b9fae-159">INPUTS</span></span>

### <span data-ttu-id="b9fae-160">Microsoft. Azure. Commands. CosmosDB. Models. PSIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="b9fae-160">Microsoft.Azure.Commands.CosmosDB.Models.PSIndexingPolicy</span></span>

### <span data-ttu-id="b9fae-161">Microsoft. Azure. Commands. CosmosDB. Models. PSUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="b9fae-161">Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKeyPolicy</span></span>

### <span data-ttu-id="b9fae-162">Microsoft. Azure. Commands. CosmosDB. Models. PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="b9fae-162">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="b9fae-163">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b9fae-163">OUTPUTS</span></span>

### <span data-ttu-id="b9fae-164">Microsoft. Azure. Commands. CosmosDB. Models. PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="b9fae-164">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

## <span data-ttu-id="b9fae-165">Notizen</span><span class="sxs-lookup"><span data-stu-id="b9fae-165">NOTES</span></span>

## <span data-ttu-id="b9fae-166">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b9fae-166">RELATED LINKS</span></span>
