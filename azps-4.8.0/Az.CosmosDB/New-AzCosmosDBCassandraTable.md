---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbcassandratable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraTable.md
ms.openlocfilehash: 42ec4db0f9c0967e375cc30a582c35aaca65840f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94167086"
---
# <span data-ttu-id="54848-101">New-AzCosmosDBCassandraTable</span><span class="sxs-lookup"><span data-stu-id="54848-101">New-AzCosmosDBCassandraTable</span></span>

## <span data-ttu-id="54848-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="54848-102">SYNOPSIS</span></span>
<span data-ttu-id="54848-103">Erstellt eine neue CosmosDB Cassandra-Tabelle.</span><span class="sxs-lookup"><span data-stu-id="54848-103">Creates a new CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="54848-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="54848-104">SYNTAX</span></span>

### <span data-ttu-id="54848-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="54848-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBCassandraTable -ResourceGroupName <String> -AccountName <String> -KeyspaceName <String>
 -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-AnalyticalStorageTtl <Int32>] -Schema <PSCassandraSchema> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="54848-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="54848-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBCassandraTable -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-TtlInSeconds <Int32>] [-AnalyticalStorageTtl <Int32>] -Schema <PSCassandraSchema>
 -ParentObject <PSCassandraKeyspaceGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="54848-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="54848-107">DESCRIPTION</span></span>
<span data-ttu-id="54848-108">Erstellt eine neue CosmosDB Cassandra-Tabelle.</span><span class="sxs-lookup"><span data-stu-id="54848-108">Creates a new CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="54848-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="54848-109">EXAMPLES</span></span>

### <span data-ttu-id="54848-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="54848-110">Example 1</span></span>
```powershell
PS C:\>       
      $Column1 = New-AzCosmosDBCassandraColumn -Name "ColumnA" -Type "int"
      $Column2 = New-AzCosmosDBCassandraColumn -Name "ColumnB" -Type "ascii"
      $Column3 = New-AzCosmosDBCassandraColumn -Name "ColumnC" -Type "int"
      $Column4 = New-AzCosmosDBCassandraColumn -Name "ColumnD" -Type "ascii"

      $clusterkey1 = New-AzCosmosDBCassandraClusterKey -Name "ColumnB" -OrderBy "Asc"
      $clusterkey2 = New-AzCosmosDBCassandraClusterKey -Name "ColumnA" -OrderBy "Asc"

      $schema = New-AzCosmosDBCassandraSchema -Column $Column1,$Column2 -ClusterKey $clusterkey1 -PartitionKey "ColumnA"

      New-AzCosmosDBCassandraTable -AccountName myAccountName -ResourceGroupName myRgName -KeyspaceName myKeyspaceName -Name myTableName -Schema $schema
        Name     : myTable
        Id       : /subscriptions/mySubId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/cassandraKeyspaces/myKeyspaceName/t
                ables/myTableName
        Location :
        Tags     :
        Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetPropertiesResource
```

## <span data-ttu-id="54848-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="54848-111">PARAMETERS</span></span>

### <span data-ttu-id="54848-112">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="54848-112">-AccountName</span></span>
<span data-ttu-id="54848-113">Name des Cosmos DB-Daten Bankkontos.</span><span class="sxs-lookup"><span data-stu-id="54848-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="54848-114">-AnalyticalStorageTtl</span><span class="sxs-lookup"><span data-stu-id="54848-114">-AnalyticalStorageTtl</span></span>
<span data-ttu-id="54848-115">Analytische Speicher TTL.</span><span class="sxs-lookup"><span data-stu-id="54848-115">Analytical Storage TTL.</span></span>

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

### <span data-ttu-id="54848-116">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="54848-116">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="54848-117">Maximaler Durchsatz, wenn "AutoScale" aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="54848-117">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="54848-118">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="54848-118">-Confirm</span></span>
<span data-ttu-id="54848-119">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="54848-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="54848-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54848-120">-DefaultProfile</span></span>
<span data-ttu-id="54848-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="54848-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="54848-122">-Keyspacename</span><span class="sxs-lookup"><span data-stu-id="54848-122">-KeyspaceName</span></span>
<span data-ttu-id="54848-123">Cassandra-Keyspace-Name.</span><span class="sxs-lookup"><span data-stu-id="54848-123">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="54848-124">-Name</span><span class="sxs-lookup"><span data-stu-id="54848-124">-Name</span></span>
<span data-ttu-id="54848-125">Cassandra-Tabellen Name.</span><span class="sxs-lookup"><span data-stu-id="54848-125">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="54848-126">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="54848-126">-ParentObject</span></span>
<span data-ttu-id="54848-127">Cassandra-Keyspace-Objekt.</span><span class="sxs-lookup"><span data-stu-id="54848-127">Cassandra Keyspace object.</span></span>

```yaml
Type: PSCassandraKeyspaceGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="54848-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54848-128">-ResourceGroupName</span></span>
<span data-ttu-id="54848-129">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="54848-129">Name of resource group.</span></span>

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

### <span data-ttu-id="54848-130">-Schema</span><span class="sxs-lookup"><span data-stu-id="54848-130">-Schema</span></span>
<span data-ttu-id="54848-131">PSCassandraSchema-Objekt.</span><span class="sxs-lookup"><span data-stu-id="54848-131">PSCassandraSchema object.</span></span>
<span data-ttu-id="54848-132">Verwenden Sie New-AzCosmosDBCassandraSchema, um dieses Objekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="54848-132">Use New-AzCosmosDBCassandraSchema to create this object.</span></span>

```yaml
Type: PSCassandraSchema
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="54848-133">-Durchsatz</span><span class="sxs-lookup"><span data-stu-id="54848-133">-Throughput</span></span>
<span data-ttu-id="54848-134">Der Durchsatz des Cassandra-Keyspace (ru/s).</span><span class="sxs-lookup"><span data-stu-id="54848-134">The throughput of Cassandra Keyspace (RU/s).</span></span>
<span data-ttu-id="54848-135">Der Standardwert ist 400.</span><span class="sxs-lookup"><span data-stu-id="54848-135">Default value is 400.</span></span>

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

### <span data-ttu-id="54848-136">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="54848-136">-TtlInSeconds</span></span>
<span data-ttu-id="54848-137">Standard-TTL in Sekunden.</span><span class="sxs-lookup"><span data-stu-id="54848-137">Default Ttl in seconds.</span></span>
<span data-ttu-id="54848-138">Wenn der Wert fehlt oder auf-1 gesetzt ist, werden die Elemente nicht ablaufen.</span><span class="sxs-lookup"><span data-stu-id="54848-138">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="54848-139">Wenn der Wert auf n gesetzt ist, werden die Elemente nach dem Zeitpunkt der letzten Änderung n Sekunden ablaufen.</span><span class="sxs-lookup"><span data-stu-id="54848-139">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="54848-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54848-140">-WhatIf</span></span>
<span data-ttu-id="54848-141">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="54848-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="54848-142">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="54848-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="54848-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54848-143">CommonParameters</span></span>
<span data-ttu-id="54848-144">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54848-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54848-145">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="54848-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54848-146">Eingaben</span><span class="sxs-lookup"><span data-stu-id="54848-146">INPUTS</span></span>

### <span data-ttu-id="54848-147">Microsoft. Azure. Commands. CosmosDB. Models. PSCassandraSchema</span><span class="sxs-lookup"><span data-stu-id="54848-147">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraSchema</span></span>

### <span data-ttu-id="54848-148">Microsoft. Azure. Commands. CosmosDB. Models. PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="54848-148">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="54848-149">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="54848-149">OUTPUTS</span></span>

### <span data-ttu-id="54848-150">Microsoft. Azure. Commands. CosmosDB. Models. PSCassandraTableGetResults</span><span class="sxs-lookup"><span data-stu-id="54848-150">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span></span>

### <span data-ttu-id="54848-151">Microsoft. Azure. Commands. CosmosDB. Exceptions. ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="54848-151">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="54848-152">Notizen</span><span class="sxs-lookup"><span data-stu-id="54848-152">NOTES</span></span>

## <span data-ttu-id="54848-153">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="54848-153">RELATED LINKS</span></span>
