---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlingraph
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinGraph.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinGraph.md
ms.openlocfilehash: ab81c97048c64a08ab29877becfd44b690312a27
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94299337"
---
# <span data-ttu-id="b22b4-101">New-AzCosmosDBGremlinGraph</span><span class="sxs-lookup"><span data-stu-id="b22b4-101">New-AzCosmosDBGremlinGraph</span></span>

## <span data-ttu-id="b22b4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b22b4-102">SYNOPSIS</span></span>
<span data-ttu-id="b22b4-103">Erstellt ein neues CosmosDB-Gremlin-Diagramm.</span><span class="sxs-lookup"><span data-stu-id="b22b4-103">Creates a new CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="b22b4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b22b4-104">SYNTAX</span></span>

### <span data-ttu-id="b22b4-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="b22b4-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBGremlinGraph -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-IndexingPolicy <PSIndexingPolicy>] [-PartitionKeyVersion <Int32>] -PartitionKeyKind <String>
 -PartitionKeyPath <String[]> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-UniqueKeyPolicy <PSUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSConflictResolutionPolicy>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b22b4-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b22b4-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBGremlinGraph -Name <String> [-IndexingPolicy <PSIndexingPolicy>] [-PartitionKeyVersion <Int32>]
 -PartitionKeyKind <String> -PartitionKeyPath <String[]> [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>] [-UniqueKeyPolicy <PSUniqueKeyPolicy>]
 [-ConflictResolutionPolicyMode <String>] [-ConflictResolutionPolicyPath <String>]
 [-ConflictResolutionPolicyProcedure <String>] [-ConflictResolutionPolicy <PSConflictResolutionPolicy>]
 -ParentObject <PSGremlinDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b22b4-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b22b4-107">DESCRIPTION</span></span>
<span data-ttu-id="b22b4-108">Erstellt ein neues CosmosDB-Gremlin-Diagramm.</span><span class="sxs-lookup"><span data-stu-id="b22b4-108">Creates a new CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="b22b4-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b22b4-109">EXAMPLES</span></span>

### <span data-ttu-id="b22b4-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b22b4-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBGremlinGraph -AccountName myAccountName -DatabaseName myDatabaseName -ResourceGroupName myRgName -Name myContainerName -PartitionKeyPath /a -PartitionKeyKind Hash

Name     : myContainerName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/gremlinDatabases/myDatabaseName/graphs/myGraphName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetPropertiesResource
```

## <span data-ttu-id="b22b4-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="b22b4-111">PARAMETERS</span></span>

### <span data-ttu-id="b22b4-112">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="b22b4-112">-AccountName</span></span>
<span data-ttu-id="b22b4-113">Name des Cosmos DB-Daten Bankkontos.</span><span class="sxs-lookup"><span data-stu-id="b22b4-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="b22b4-114">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="b22b4-114">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="b22b4-115">Maximaler Durchsatz, wenn "AutoScale" aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="b22b4-115">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="b22b4-116">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b22b4-116">-Confirm</span></span>
<span data-ttu-id="b22b4-117">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b22b4-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b22b4-118">-ConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="b22b4-118">-ConflictResolutionPolicy</span></span>
<span data-ttu-id="b22b4-119">ConflictResolutionPolicy-Objekt vom Typ PSConflictResolutionPolicy, wenn diese Einstellung als ConflictResolutionPolicy des Containers angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="b22b4-119">ConflictResolutionPolicy Object of type PSConflictResolutionPolicy, when provided this is set as the ConflictResolutionPolicy of the container.</span></span>

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

### <span data-ttu-id="b22b4-120">-ConflictResolutionPolicyMode</span><span class="sxs-lookup"><span data-stu-id="b22b4-120">-ConflictResolutionPolicyMode</span></span>
<span data-ttu-id="b22b4-121">Kann die Werte haben: LastWriterWins, Benutzerdefiniert, manuell.</span><span class="sxs-lookup"><span data-stu-id="b22b4-121">Can have the values: LastWriterWins, Custom, Manual.</span></span>

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

### <span data-ttu-id="b22b4-122">-ConflictResolutionPolicyPath</span><span class="sxs-lookup"><span data-stu-id="b22b4-122">-ConflictResolutionPolicyPath</span></span>
<span data-ttu-id="b22b4-123">, Die bereitgestellt werden soll, wenn der Typ LastWriterWins ist.</span><span class="sxs-lookup"><span data-stu-id="b22b4-123">To be provided when the type is LastWriterWins.</span></span>

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

### <span data-ttu-id="b22b4-124">-ConflictResolutionPolicyProcedure</span><span class="sxs-lookup"><span data-stu-id="b22b4-124">-ConflictResolutionPolicyProcedure</span></span>
<span data-ttu-id="b22b4-125">, Die bereitgestellt werden soll, wenn der Typ Benutzerdefiniert ist.</span><span class="sxs-lookup"><span data-stu-id="b22b4-125">To be provided when the type is custom.</span></span>

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

### <span data-ttu-id="b22b4-126">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b22b4-126">-DatabaseName</span></span>
<span data-ttu-id="b22b4-127">Datenbankname</span><span class="sxs-lookup"><span data-stu-id="b22b4-127">Database name.</span></span>

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

### <span data-ttu-id="b22b4-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b22b4-128">-DefaultProfile</span></span>
<span data-ttu-id="b22b4-129">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b22b4-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b22b4-130">-IndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="b22b4-130">-IndexingPolicy</span></span>
<span data-ttu-id="b22b4-131">Indizierungs Richtlinienobjekt vom Typ Microsoft. Azure. Commands. CosmosDB. PSIndexingPolicy.</span><span class="sxs-lookup"><span data-stu-id="b22b4-131">Indexing Policy Object of type Microsoft.Azure.Commands.CosmosDB.PSIndexingPolicy.</span></span>

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

### <span data-ttu-id="b22b4-132">-Name</span><span class="sxs-lookup"><span data-stu-id="b22b4-132">-Name</span></span>
<span data-ttu-id="b22b4-133">Gremlin-Diagramm Name</span><span class="sxs-lookup"><span data-stu-id="b22b4-133">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="b22b4-134">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="b22b4-134">-ParentObject</span></span>
<span data-ttu-id="b22b4-135">Gremlin-Datenbankobjekt.</span><span class="sxs-lookup"><span data-stu-id="b22b4-135">Gremlin Database object.</span></span>

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

### <span data-ttu-id="b22b4-136">-PartitionKeyKind</span><span class="sxs-lookup"><span data-stu-id="b22b4-136">-PartitionKeyKind</span></span>
<span data-ttu-id="b22b4-137">Die Art des für die Partitionierung verwendeten Algorithmus.</span><span class="sxs-lookup"><span data-stu-id="b22b4-137">The kind of algorithm used for partitioning.</span></span>
<span data-ttu-id="b22b4-138">Mögliche Werte sind: "Hash"; "Bereich"</span><span class="sxs-lookup"><span data-stu-id="b22b4-138">Possible values include: 'Hash', 'Range'</span></span>

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

### <span data-ttu-id="b22b4-139">-PartitionKeyPath</span><span class="sxs-lookup"><span data-stu-id="b22b4-139">-PartitionKeyPath</span></span>
<span data-ttu-id="b22b4-140">Partitionsschlüssel Pfad, beispielsweise "/Address/ZipCode".</span><span class="sxs-lookup"><span data-stu-id="b22b4-140">Partition Key Path, e.g., '/address/zipcode'.</span></span>

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

### <span data-ttu-id="b22b4-141">-PartitionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="b22b4-141">-PartitionKeyVersion</span></span>
<span data-ttu-id="b22b4-142">Die Version der Partitionsschlüssel Definition</span><span class="sxs-lookup"><span data-stu-id="b22b4-142">The version of the partition key definition</span></span>

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

### <span data-ttu-id="b22b4-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b22b4-143">-ResourceGroupName</span></span>
<span data-ttu-id="b22b4-144">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="b22b4-144">Name of resource group.</span></span>

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

### <span data-ttu-id="b22b4-145">-Durchsatz</span><span class="sxs-lookup"><span data-stu-id="b22b4-145">-Throughput</span></span>
<span data-ttu-id="b22b4-146">Der Durchsatz von Gremlin Graph (ru/s).</span><span class="sxs-lookup"><span data-stu-id="b22b4-146">The throughput of Gremlin Graph (RU/s).</span></span>
<span data-ttu-id="b22b4-147">Der Standardwert ist 400.</span><span class="sxs-lookup"><span data-stu-id="b22b4-147">Default value is 400.</span></span>

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

### <span data-ttu-id="b22b4-148">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="b22b4-148">-TtlInSeconds</span></span>
<span data-ttu-id="b22b4-149">Standard-TTL in Sekunden.</span><span class="sxs-lookup"><span data-stu-id="b22b4-149">Default Ttl in seconds.</span></span>
<span data-ttu-id="b22b4-150">Wenn der Wert fehlt oder auf-1 gesetzt ist, werden die Elemente nicht ablaufen.</span><span class="sxs-lookup"><span data-stu-id="b22b4-150">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="b22b4-151">Wenn der Wert auf n gesetzt ist, werden die Elemente nach dem Zeitpunkt der letzten Änderung n Sekunden ablaufen.</span><span class="sxs-lookup"><span data-stu-id="b22b4-151">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="b22b4-152">-UniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="b22b4-152">-UniqueKeyPolicy</span></span>
<span data-ttu-id="b22b4-153">UniqueKeyPolicy-Objekt vom Typ Microsoft. Azure. Commands. CosmosDB. PSUniqueKeyPolicy.</span><span class="sxs-lookup"><span data-stu-id="b22b4-153">UniqueKeyPolicy Object of type Microsoft.Azure.Commands.CosmosDB.PSUniqueKeyPolicy.</span></span>

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

### <span data-ttu-id="b22b4-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b22b4-154">-WhatIf</span></span>
<span data-ttu-id="b22b4-155">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b22b4-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b22b4-156">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b22b4-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b22b4-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b22b4-157">CommonParameters</span></span>
<span data-ttu-id="b22b4-158">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b22b4-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b22b4-159">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b22b4-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b22b4-160">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b22b4-160">INPUTS</span></span>

### <span data-ttu-id="b22b4-161">Microsoft. Azure. Commands. CosmosDB. Models. PSIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="b22b4-161">Microsoft.Azure.Commands.CosmosDB.Models.PSIndexingPolicy</span></span>

### <span data-ttu-id="b22b4-162">Microsoft. Azure. Commands. CosmosDB. Models. PSUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="b22b4-162">Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKeyPolicy</span></span>

### <span data-ttu-id="b22b4-163">Microsoft. Azure. Commands. CosmosDB. Models. PSConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="b22b4-163">Microsoft.Azure.Commands.CosmosDB.Models.PSConflictResolutionPolicy</span></span>

### <span data-ttu-id="b22b4-164">Microsoft. Azure. Commands. CosmosDB. Models. PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="b22b4-164">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="b22b4-165">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b22b4-165">OUTPUTS</span></span>

### <span data-ttu-id="b22b4-166">Microsoft. Azure. Commands. CosmosDB. Models. PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="b22b4-166">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

### <span data-ttu-id="b22b4-167">System. Exception</span><span class="sxs-lookup"><span data-stu-id="b22b4-167">System.Exception</span></span>

## <span data-ttu-id="b22b4-168">Notizen</span><span class="sxs-lookup"><span data-stu-id="b22b4-168">NOTES</span></span>

## <span data-ttu-id="b22b4-169">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b22b4-169">RELATED LINKS</span></span>
