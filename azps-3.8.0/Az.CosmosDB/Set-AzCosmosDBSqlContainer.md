---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/set-azcosmosdbsqlcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBSqlContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBSqlContainer.md
ms.openlocfilehash: 83c26ff0a05a88540563b7e3867c2e1d6ac12be0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94004631"
---
# <span data-ttu-id="68b97-101">Set-AzCosmosDBSqlContainer</span><span class="sxs-lookup"><span data-stu-id="68b97-101">Set-AzCosmosDBSqlContainer</span></span>

## <span data-ttu-id="68b97-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="68b97-102">SYNOPSIS</span></span>
<span data-ttu-id="68b97-103">Erstellt eine neue oder aktualisiert einen vorhandenen CosmosDB-SQL-Container.</span><span class="sxs-lookup"><span data-stu-id="68b97-103">Creates a new or updates an existing CosmosDB Sql Container.</span></span>

## <span data-ttu-id="68b97-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="68b97-104">SYNTAX</span></span>

### <span data-ttu-id="68b97-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="68b97-105">ByNameParameterSet (Default)</span></span>
```
Set-AzCosmosDBSqlContainer -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-IndexingPolicy <PSSqlIndexingPolicy>] [-PartitionKeyVersion <Int32>]
 -PartitionKeyKind <String> -PartitionKeyPath <String[]> [-Throughput <Int32>] [-TtlInSeconds <Int32>]
 [-UniqueKeyPolicy <PSSqlUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSSqlConflictResolutionPolicy>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="68b97-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="68b97-106">ByParentObjectParameterSet</span></span>
```
Set-AzCosmosDBSqlContainer -Name <String> [-IndexingPolicy <PSSqlIndexingPolicy>]
 [-PartitionKeyVersion <Int32>] -PartitionKeyKind <String> -PartitionKeyPath <String[]> [-Throughput <Int32>]
 [-TtlInSeconds <Int32>] [-UniqueKeyPolicy <PSSqlUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSSqlConflictResolutionPolicy>] -InputObject <PSSqlDatabaseGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="68b97-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="68b97-107">DESCRIPTION</span></span>
<span data-ttu-id="68b97-108">Das Cmdlet " **Satz-AzCosmosDBSqlContainer** " erstellt ein neues oder aktualisiert einen vorhandenen CosmosDB SQL-Container.</span><span class="sxs-lookup"><span data-stu-id="68b97-108">The **Set-AzCosmosDBSqlContainer** cmdlet creates a new or updates an existing CosmosDB Sql Container.</span></span>

## <span data-ttu-id="68b97-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="68b97-109">EXAMPLES</span></span>

### <span data-ttu-id="68b97-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="68b97-110">Example 1</span></span>
```powershell
PS C:\> Set-AzCosmosDBSqlContainer -ResourceGroupName {resourceGroupName} -AccountName {accountName} -DatabaseName {databaseName} -Name {containerName} -PartitionKeyKind Hash -PartitionKeyPath {samplePath}

Name                     : {containerName}
Id                       : {containerId}
Resource                 : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetPropertiesResource
```

## <span data-ttu-id="68b97-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="68b97-111">PARAMETERS</span></span>

### <span data-ttu-id="68b97-112">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="68b97-112">-AccountName</span></span>
<span data-ttu-id="68b97-113">Name des Cosmos DB-Daten Bankkontos.</span><span class="sxs-lookup"><span data-stu-id="68b97-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="68b97-114">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="68b97-114">-Confirm</span></span>
<span data-ttu-id="68b97-115">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="68b97-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="68b97-116">-ConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="68b97-116">-ConflictResolutionPolicy</span></span>
<span data-ttu-id="68b97-117">ConflictResolutionPolicy-Objekt vom Typ PSSqlConflictResolutionPolicy, wenn diese Einstellung als ConflictResolutionPolicy des Containers angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="68b97-117">ConflictResolutionPolicy Object of type PSSqlConflictResolutionPolicy, when provided this is set as the ConflictResolutionPolicy of the container.</span></span>

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

### <span data-ttu-id="68b97-118">-ConflictResolutionPolicyMode</span><span class="sxs-lookup"><span data-stu-id="68b97-118">-ConflictResolutionPolicyMode</span></span>
<span data-ttu-id="68b97-119">Kann die Werte haben: LastWriterWins, Benutzerdefiniert, manuell.</span><span class="sxs-lookup"><span data-stu-id="68b97-119">Can have the values: LastWriterWins, Custom, Manual.</span></span>

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

### <span data-ttu-id="68b97-120">-ConflictResolutionPolicyPath</span><span class="sxs-lookup"><span data-stu-id="68b97-120">-ConflictResolutionPolicyPath</span></span>
<span data-ttu-id="68b97-121">, Die bereitgestellt werden soll, wenn der Typ LastWriterWins ist.</span><span class="sxs-lookup"><span data-stu-id="68b97-121">To be provided when the type is LastWriterWins.</span></span>

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

### <span data-ttu-id="68b97-122">-ConflictResolutionPolicyProcedure</span><span class="sxs-lookup"><span data-stu-id="68b97-122">-ConflictResolutionPolicyProcedure</span></span>
<span data-ttu-id="68b97-123">, Die bereitgestellt werden soll, wenn der Typ Benutzerdefiniert ist.</span><span class="sxs-lookup"><span data-stu-id="68b97-123">To be provided when the type is custom.</span></span>

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

### <span data-ttu-id="68b97-124">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="68b97-124">-DatabaseName</span></span>
<span data-ttu-id="68b97-125">Datenbankname</span><span class="sxs-lookup"><span data-stu-id="68b97-125">Database name.</span></span>

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

### <span data-ttu-id="68b97-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68b97-126">-DefaultProfile</span></span>
<span data-ttu-id="68b97-127">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="68b97-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="68b97-128">-IndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="68b97-128">-IndexingPolicy</span></span>
<span data-ttu-id="68b97-129">Indizierungs Richtlinienobjekt vom Typ Microsoft. Azure. Commands. CosmosDB. PSSqlIndexingPolicy.</span><span class="sxs-lookup"><span data-stu-id="68b97-129">Indexing Policy Object of type Microsoft.Azure.Commands.CosmosDB.PSSqlIndexingPolicy.</span></span>

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

### <span data-ttu-id="68b97-130">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="68b97-130">-InputObject</span></span>
<span data-ttu-id="68b97-131">SQL-Datenbankobjekt.</span><span class="sxs-lookup"><span data-stu-id="68b97-131">Sql Database object.</span></span>

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

### <span data-ttu-id="68b97-132">-Name</span><span class="sxs-lookup"><span data-stu-id="68b97-132">-Name</span></span>
<span data-ttu-id="68b97-133">Container Name.</span><span class="sxs-lookup"><span data-stu-id="68b97-133">Container name.</span></span>

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

### <span data-ttu-id="68b97-134">-PartitionKeyKind</span><span class="sxs-lookup"><span data-stu-id="68b97-134">-PartitionKeyKind</span></span>
<span data-ttu-id="68b97-135">Die Art des für die Partitionierung verwendeten Algorithmus.</span><span class="sxs-lookup"><span data-stu-id="68b97-135">The kind of algorithm used for partitioning.</span></span>
<span data-ttu-id="68b97-136">Mögliche Werte sind: "Hash"; "Bereich"</span><span class="sxs-lookup"><span data-stu-id="68b97-136">Possible values include: 'Hash', 'Range'</span></span>

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

### <span data-ttu-id="68b97-137">-PartitionKeyPath</span><span class="sxs-lookup"><span data-stu-id="68b97-137">-PartitionKeyPath</span></span>
<span data-ttu-id="68b97-138">Partitionsschlüssel Pfad, beispielsweise "/Address/ZipCode".</span><span class="sxs-lookup"><span data-stu-id="68b97-138">Partition Key Path, e.g., '/address/zipcode'.</span></span>

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

### <span data-ttu-id="68b97-139">-PartitionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="68b97-139">-PartitionKeyVersion</span></span>
<span data-ttu-id="68b97-140">Die Version der Partitionsschlüssel Definition</span><span class="sxs-lookup"><span data-stu-id="68b97-140">The version of the partition key definition</span></span>

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

### <span data-ttu-id="68b97-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68b97-141">-ResourceGroupName</span></span>
<span data-ttu-id="68b97-142">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="68b97-142">Name of resource group.</span></span>

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

### <span data-ttu-id="68b97-143">-Durchsatz</span><span class="sxs-lookup"><span data-stu-id="68b97-143">-Throughput</span></span>
<span data-ttu-id="68b97-144">Der Durchsatz des SQL-Containers (ru/s).</span><span class="sxs-lookup"><span data-stu-id="68b97-144">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="68b97-145">Der Standardwert ist 400.</span><span class="sxs-lookup"><span data-stu-id="68b97-145">Default value is 400.</span></span>

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

### <span data-ttu-id="68b97-146">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="68b97-146">-TtlInSeconds</span></span>
<span data-ttu-id="68b97-147">Standard-TTL in Sekunden.</span><span class="sxs-lookup"><span data-stu-id="68b97-147">Default Ttl in seconds.</span></span>
<span data-ttu-id="68b97-148">Wenn der Wert fehlt oder auf-1 gesetzt ist, werden die Elemente nicht ablaufen.</span><span class="sxs-lookup"><span data-stu-id="68b97-148">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="68b97-149">Wenn der Wert auf n gesetzt ist, werden die Elemente nach dem Zeitpunkt der letzten Änderung n Sekunden ablaufen.</span><span class="sxs-lookup"><span data-stu-id="68b97-149">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="68b97-150">-UniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="68b97-150">-UniqueKeyPolicy</span></span>
<span data-ttu-id="68b97-151">UniqueKeyPolicy-Objekt vom Typ Microsoft. Azure. Commands. CosmosDB. PSSqlUniqueKeyPolicy.</span><span class="sxs-lookup"><span data-stu-id="68b97-151">UniqueKeyPolicy Object of type Microsoft.Azure.Commands.CosmosDB.PSSqlUniqueKeyPolicy.</span></span>

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

### <span data-ttu-id="68b97-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="68b97-152">-WhatIf</span></span>
<span data-ttu-id="68b97-153">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="68b97-153">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="68b97-154">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="68b97-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="68b97-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68b97-155">CommonParameters</span></span>
<span data-ttu-id="68b97-156">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68b97-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68b97-157">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="68b97-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68b97-158">Eingaben</span><span class="sxs-lookup"><span data-stu-id="68b97-158">INPUTS</span></span>

### <span data-ttu-id="68b97-159">Keine</span><span class="sxs-lookup"><span data-stu-id="68b97-159">None</span></span>

## <span data-ttu-id="68b97-160">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="68b97-160">OUTPUTS</span></span>

### <span data-ttu-id="68b97-161">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="68b97-161">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

## <span data-ttu-id="68b97-162">Notizen</span><span class="sxs-lookup"><span data-stu-id="68b97-162">NOTES</span></span>

## <span data-ttu-id="68b97-163">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="68b97-163">RELATED LINKS</span></span>
