---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbcassandratable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraTable.md
ms.openlocfilehash: 7251b4b928bb0adc94bc42da9d5bcef063c86259
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101946616"
---
# <span data-ttu-id="2ede0-101">New-AzCosmosDBCassandraTable</span><span class="sxs-lookup"><span data-stu-id="2ede0-101">New-AzCosmosDBCassandraTable</span></span>

## <span data-ttu-id="2ede0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2ede0-102">SYNOPSIS</span></span>
<span data-ttu-id="2ede0-103">Erstellt eine neue CosmosDB-Kassandratabelle.</span><span class="sxs-lookup"><span data-stu-id="2ede0-103">Creates a new CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="2ede0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2ede0-104">SYNTAX</span></span>

### <span data-ttu-id="2ede0-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="2ede0-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBCassandraTable -ResourceGroupName <String> -AccountName <String> -KeyspaceName <String>
 -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-AnalyticalStorageTtl <Int32>] -Schema <PSCassandraSchema> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2ede0-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2ede0-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBCassandraTable -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-TtlInSeconds <Int32>] [-AnalyticalStorageTtl <Int32>] -Schema <PSCassandraSchema>
 -ParentObject <PSCassandraKeyspaceGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2ede0-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2ede0-107">DESCRIPTION</span></span>
<span data-ttu-id="2ede0-108">Erstellt eine neue CosmosDB-Kassandratabelle.</span><span class="sxs-lookup"><span data-stu-id="2ede0-108">Creates a new CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="2ede0-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2ede0-109">EXAMPLES</span></span>

### <span data-ttu-id="2ede0-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2ede0-110">Example 1</span></span>
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

## <span data-ttu-id="2ede0-111">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="2ede0-111">PARAMETERS</span></span>

### <span data-ttu-id="2ede0-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="2ede0-112">-AccountName</span></span>
<span data-ttu-id="2ede0-113">Name des Datenbankkontos "Cosmos DB".</span><span class="sxs-lookup"><span data-stu-id="2ede0-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="2ede0-114">-AnalyticalStorageTtl</span><span class="sxs-lookup"><span data-stu-id="2ede0-114">-AnalyticalStorageTtl</span></span>
<span data-ttu-id="2ede0-115">TTL für analytischen Speicher.</span><span class="sxs-lookup"><span data-stu-id="2ede0-115">Analytical Storage TTL.</span></span>

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

### <span data-ttu-id="2ede0-116">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="2ede0-116">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="2ede0-117">Maximaler Durchsatzwert, wenn die automatische Skalierung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="2ede0-117">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="2ede0-118">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2ede0-118">-Confirm</span></span>
<span data-ttu-id="2ede0-119">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2ede0-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2ede0-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ede0-120">-DefaultProfile</span></span>
<span data-ttu-id="2ede0-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2ede0-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2ede0-122">-KeyspaceName</span><span class="sxs-lookup"><span data-stu-id="2ede0-122">-KeyspaceName</span></span>
<span data-ttu-id="2ede0-123">Name des Kassa-Schlüsselbereichs.</span><span class="sxs-lookup"><span data-stu-id="2ede0-123">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="2ede0-124">-Name</span><span class="sxs-lookup"><span data-stu-id="2ede0-124">-Name</span></span>
<span data-ttu-id="2ede0-125">Name der Tabelle "Kassandra".</span><span class="sxs-lookup"><span data-stu-id="2ede0-125">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="2ede0-126">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="2ede0-126">-ParentObject</span></span>
<span data-ttu-id="2ede0-127">Das Objekt "Kassandra-Keyspace".</span><span class="sxs-lookup"><span data-stu-id="2ede0-127">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="2ede0-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ede0-128">-ResourceGroupName</span></span>
<span data-ttu-id="2ede0-129">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="2ede0-129">Name of resource group.</span></span>

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

### <span data-ttu-id="2ede0-130">-Schema</span><span class="sxs-lookup"><span data-stu-id="2ede0-130">-Schema</span></span>
<span data-ttu-id="2ede0-131">PSCassandraSchema-Objekt.</span><span class="sxs-lookup"><span data-stu-id="2ede0-131">PSCassandraSchema object.</span></span>
<span data-ttu-id="2ede0-132">Verwenden New-AzCosmosDBCassandraSchema, um dieses Objekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="2ede0-132">Use New-AzCosmosDBCassandraSchema to create this object.</span></span>

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

### <span data-ttu-id="2ede0-133">-Durchsatz</span><span class="sxs-lookup"><span data-stu-id="2ede0-133">-Throughput</span></span>
<span data-ttu-id="2ede0-134">Der Durchsatz von Cassisy Keyspace (RU/s).</span><span class="sxs-lookup"><span data-stu-id="2ede0-134">The throughput of Cassandra Keyspace (RU/s).</span></span>
<span data-ttu-id="2ede0-135">Der Standardwert ist 400.</span><span class="sxs-lookup"><span data-stu-id="2ede0-135">Default value is 400.</span></span>

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

### <span data-ttu-id="2ede0-136">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="2ede0-136">-TtlInSeconds</span></span>
<span data-ttu-id="2ede0-137">Standard-Ttl in Sekunden.</span><span class="sxs-lookup"><span data-stu-id="2ede0-137">Default Ttl in seconds.</span></span>
<span data-ttu-id="2ede0-138">Wenn der Wert fehlt oder auf - 1 festgelegt ist, laufen die Elemente nicht ab.</span><span class="sxs-lookup"><span data-stu-id="2ede0-138">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="2ede0-139">Wenn der Wert auf n festgelegt ist, laufen Elemente n Sekunden nach der letzten Änderungszeit ab.</span><span class="sxs-lookup"><span data-stu-id="2ede0-139">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="2ede0-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ede0-140">-WhatIf</span></span>
<span data-ttu-id="2ede0-141">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2ede0-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2ede0-142">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2ede0-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2ede0-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ede0-143">CommonParameters</span></span>
<span data-ttu-id="2ede0-144">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ede0-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ede0-145">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2ede0-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ede0-146">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2ede0-146">INPUTS</span></span>

### <span data-ttu-id="2ede0-147">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraSchema</span><span class="sxs-lookup"><span data-stu-id="2ede0-147">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraSchema</span></span>

### <span data-ttu-id="2ede0-148">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="2ede0-148">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="2ede0-149">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2ede0-149">OUTPUTS</span></span>

### <span data-ttu-id="2ede0-150">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span><span class="sxs-lookup"><span data-stu-id="2ede0-150">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span></span>

### <span data-ttu-id="2ede0-151">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="2ede0-151">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="2ede0-152">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="2ede0-152">NOTES</span></span>

## <span data-ttu-id="2ede0-153">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="2ede0-153">RELATED LINKS</span></span>
