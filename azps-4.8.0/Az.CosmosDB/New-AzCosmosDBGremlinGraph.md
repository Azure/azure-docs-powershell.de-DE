---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlingraph
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinGraph.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinGraph.md
ms.openlocfilehash: ab81c97048c64a08ab29877becfd44b690312a27
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94173076"
---
# <span data-ttu-id="5e0de-101">New-AzCosmosDBGremlinGraph</span><span class="sxs-lookup"><span data-stu-id="5e0de-101">New-AzCosmosDBGremlinGraph</span></span>

## <span data-ttu-id="5e0de-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5e0de-102">SYNOPSIS</span></span>
<span data-ttu-id="5e0de-103">Erstellt ein neues CosmosDB-Gremlin-Diagramm.</span><span class="sxs-lookup"><span data-stu-id="5e0de-103">Creates a new CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="5e0de-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5e0de-104">SYNTAX</span></span>

### <span data-ttu-id="5e0de-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="5e0de-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBGremlinGraph -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-IndexingPolicy <PSIndexingPolicy>] [-PartitionKeyVersion <Int32>] -PartitionKeyKind <String>
 -PartitionKeyPath <String[]> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-UniqueKeyPolicy <PSUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSConflictResolutionPolicy>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e0de-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5e0de-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBGremlinGraph -Name <String> [-IndexingPolicy <PSIndexingPolicy>] [-PartitionKeyVersion <Int32>]
 -PartitionKeyKind <String> -PartitionKeyPath <String[]> [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>] [-UniqueKeyPolicy <PSUniqueKeyPolicy>]
 [-ConflictResolutionPolicyMode <String>] [-ConflictResolutionPolicyPath <String>]
 [-ConflictResolutionPolicyProcedure <String>] [-ConflictResolutionPolicy <PSConflictResolutionPolicy>]
 -ParentObject <PSGremlinDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5e0de-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5e0de-107">DESCRIPTION</span></span>
<span data-ttu-id="5e0de-108">Erstellt ein neues CosmosDB-Gremlin-Diagramm.</span><span class="sxs-lookup"><span data-stu-id="5e0de-108">Creates a new CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="5e0de-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5e0de-109">EXAMPLES</span></span>

### <span data-ttu-id="5e0de-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5e0de-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBGremlinGraph -AccountName myAccountName -DatabaseName myDatabaseName -ResourceGroupName myRgName -Name myContainerName -PartitionKeyPath /a -PartitionKeyKind Hash

Name     : myContainerName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/gremlinDatabases/myDatabaseName/graphs/myGraphName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetPropertiesResource
```

## <span data-ttu-id="5e0de-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="5e0de-111">PARAMETERS</span></span>

### <span data-ttu-id="5e0de-112">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="5e0de-112">-AccountName</span></span>
<span data-ttu-id="5e0de-113">Name des Cosmos DB-Daten Bankkontos.</span><span class="sxs-lookup"><span data-stu-id="5e0de-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="5e0de-114">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="5e0de-114">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="5e0de-115">Maximaler Durchsatz, wenn "AutoScale" aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="5e0de-115">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="5e0de-116">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5e0de-116">-Confirm</span></span>
<span data-ttu-id="5e0de-117">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5e0de-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e0de-118">-ConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="5e0de-118">-ConflictResolutionPolicy</span></span>
<span data-ttu-id="5e0de-119">ConflictResolutionPolicy-Objekt vom Typ PSConflictResolutionPolicy, wenn diese Einstellung als ConflictResolutionPolicy des Containers angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="5e0de-119">ConflictResolutionPolicy Object of type PSConflictResolutionPolicy, when provided this is set as the ConflictResolutionPolicy of the container.</span></span>

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

### <span data-ttu-id="5e0de-120">-ConflictResolutionPolicyMode</span><span class="sxs-lookup"><span data-stu-id="5e0de-120">-ConflictResolutionPolicyMode</span></span>
<span data-ttu-id="5e0de-121">Kann die Werte haben: LastWriterWins, Benutzerdefiniert, manuell.</span><span class="sxs-lookup"><span data-stu-id="5e0de-121">Can have the values: LastWriterWins, Custom, Manual.</span></span>

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

### <span data-ttu-id="5e0de-122">-ConflictResolutionPolicyPath</span><span class="sxs-lookup"><span data-stu-id="5e0de-122">-ConflictResolutionPolicyPath</span></span>
<span data-ttu-id="5e0de-123">, Die bereitgestellt werden soll, wenn der Typ LastWriterWins ist.</span><span class="sxs-lookup"><span data-stu-id="5e0de-123">To be provided when the type is LastWriterWins.</span></span>

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

### <span data-ttu-id="5e0de-124">-ConflictResolutionPolicyProcedure</span><span class="sxs-lookup"><span data-stu-id="5e0de-124">-ConflictResolutionPolicyProcedure</span></span>
<span data-ttu-id="5e0de-125">, Die bereitgestellt werden soll, wenn der Typ Benutzerdefiniert ist.</span><span class="sxs-lookup"><span data-stu-id="5e0de-125">To be provided when the type is custom.</span></span>

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

### <span data-ttu-id="5e0de-126">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="5e0de-126">-DatabaseName</span></span>
<span data-ttu-id="5e0de-127">Datenbankname</span><span class="sxs-lookup"><span data-stu-id="5e0de-127">Database name.</span></span>

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

### <span data-ttu-id="5e0de-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e0de-128">-DefaultProfile</span></span>
<span data-ttu-id="5e0de-129">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5e0de-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5e0de-130">-IndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="5e0de-130">-IndexingPolicy</span></span>
<span data-ttu-id="5e0de-131">Indizierungs Richtlinienobjekt vom Typ Microsoft. Azure. Commands. CosmosDB. PSIndexingPolicy.</span><span class="sxs-lookup"><span data-stu-id="5e0de-131">Indexing Policy Object of type Microsoft.Azure.Commands.CosmosDB.PSIndexingPolicy.</span></span>

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

### <span data-ttu-id="5e0de-132">-Name</span><span class="sxs-lookup"><span data-stu-id="5e0de-132">-Name</span></span>
<span data-ttu-id="5e0de-133">Gremlin-Diagramm Name</span><span class="sxs-lookup"><span data-stu-id="5e0de-133">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="5e0de-134">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="5e0de-134">-ParentObject</span></span>
<span data-ttu-id="5e0de-135">Gremlin-Datenbankobjekt.</span><span class="sxs-lookup"><span data-stu-id="5e0de-135">Gremlin Database object.</span></span>

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

### <span data-ttu-id="5e0de-136">-PartitionKeyKind</span><span class="sxs-lookup"><span data-stu-id="5e0de-136">-PartitionKeyKind</span></span>
<span data-ttu-id="5e0de-137">Die Art des für die Partitionierung verwendeten Algorithmus.</span><span class="sxs-lookup"><span data-stu-id="5e0de-137">The kind of algorithm used for partitioning.</span></span>
<span data-ttu-id="5e0de-138">Mögliche Werte sind: "Hash"; "Bereich"</span><span class="sxs-lookup"><span data-stu-id="5e0de-138">Possible values include: 'Hash', 'Range'</span></span>

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

### <span data-ttu-id="5e0de-139">-PartitionKeyPath</span><span class="sxs-lookup"><span data-stu-id="5e0de-139">-PartitionKeyPath</span></span>
<span data-ttu-id="5e0de-140">Partitionsschlüssel Pfad, beispielsweise "/Address/ZipCode".</span><span class="sxs-lookup"><span data-stu-id="5e0de-140">Partition Key Path, e.g., '/address/zipcode'.</span></span>

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

### <span data-ttu-id="5e0de-141">-PartitionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="5e0de-141">-PartitionKeyVersion</span></span>
<span data-ttu-id="5e0de-142">Die Version der Partitionsschlüssel Definition</span><span class="sxs-lookup"><span data-stu-id="5e0de-142">The version of the partition key definition</span></span>

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

### <span data-ttu-id="5e0de-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e0de-143">-ResourceGroupName</span></span>
<span data-ttu-id="5e0de-144">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="5e0de-144">Name of resource group.</span></span>

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

### <span data-ttu-id="5e0de-145">-Durchsatz</span><span class="sxs-lookup"><span data-stu-id="5e0de-145">-Throughput</span></span>
<span data-ttu-id="5e0de-146">Der Durchsatz von Gremlin Graph (ru/s).</span><span class="sxs-lookup"><span data-stu-id="5e0de-146">The throughput of Gremlin Graph (RU/s).</span></span>
<span data-ttu-id="5e0de-147">Der Standardwert ist 400.</span><span class="sxs-lookup"><span data-stu-id="5e0de-147">Default value is 400.</span></span>

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

### <span data-ttu-id="5e0de-148">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="5e0de-148">-TtlInSeconds</span></span>
<span data-ttu-id="5e0de-149">Standard-TTL in Sekunden.</span><span class="sxs-lookup"><span data-stu-id="5e0de-149">Default Ttl in seconds.</span></span>
<span data-ttu-id="5e0de-150">Wenn der Wert fehlt oder auf-1 gesetzt ist, werden die Elemente nicht ablaufen.</span><span class="sxs-lookup"><span data-stu-id="5e0de-150">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="5e0de-151">Wenn der Wert auf n gesetzt ist, werden die Elemente nach dem Zeitpunkt der letzten Änderung n Sekunden ablaufen.</span><span class="sxs-lookup"><span data-stu-id="5e0de-151">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="5e0de-152">-UniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="5e0de-152">-UniqueKeyPolicy</span></span>
<span data-ttu-id="5e0de-153">UniqueKeyPolicy-Objekt vom Typ Microsoft. Azure. Commands. CosmosDB. PSUniqueKeyPolicy.</span><span class="sxs-lookup"><span data-stu-id="5e0de-153">UniqueKeyPolicy Object of type Microsoft.Azure.Commands.CosmosDB.PSUniqueKeyPolicy.</span></span>

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

### <span data-ttu-id="5e0de-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e0de-154">-WhatIf</span></span>
<span data-ttu-id="5e0de-155">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5e0de-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5e0de-156">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5e0de-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e0de-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e0de-157">CommonParameters</span></span>
<span data-ttu-id="5e0de-158">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e0de-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e0de-159">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5e0de-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e0de-160">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5e0de-160">INPUTS</span></span>

### <span data-ttu-id="5e0de-161">Microsoft. Azure. Commands. CosmosDB. Models. PSIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="5e0de-161">Microsoft.Azure.Commands.CosmosDB.Models.PSIndexingPolicy</span></span>

### <span data-ttu-id="5e0de-162">Microsoft. Azure. Commands. CosmosDB. Models. PSUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="5e0de-162">Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKeyPolicy</span></span>

### <span data-ttu-id="5e0de-163">Microsoft. Azure. Commands. CosmosDB. Models. PSConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="5e0de-163">Microsoft.Azure.Commands.CosmosDB.Models.PSConflictResolutionPolicy</span></span>

### <span data-ttu-id="5e0de-164">Microsoft. Azure. Commands. CosmosDB. Models. PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="5e0de-164">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="5e0de-165">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5e0de-165">OUTPUTS</span></span>

### <span data-ttu-id="5e0de-166">Microsoft. Azure. Commands. CosmosDB. Models. PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="5e0de-166">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

### <span data-ttu-id="5e0de-167">System. Exception</span><span class="sxs-lookup"><span data-stu-id="5e0de-167">System.Exception</span></span>

## <span data-ttu-id="5e0de-168">Notizen</span><span class="sxs-lookup"><span data-stu-id="5e0de-168">NOTES</span></span>

## <span data-ttu-id="5e0de-169">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5e0de-169">RELATED LINKS</span></span>
