---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbcassandratable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraTable.md
ms.openlocfilehash: 42ec4db0f9c0967e375cc30a582c35aaca65840f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98297592"
---
# <span data-ttu-id="f28ac-101">New-AzCosmosDBCassandraTable</span><span class="sxs-lookup"><span data-stu-id="f28ac-101">New-AzCosmosDBCassandraTable</span></span>

## <span data-ttu-id="f28ac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f28ac-102">SYNOPSIS</span></span>
<span data-ttu-id="f28ac-103">Erstellt eine neue Tabelle des Unterndb-Unternings.</span><span class="sxs-lookup"><span data-stu-id="f28ac-103">Creates a new CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="f28ac-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f28ac-104">SYNTAX</span></span>

### <span data-ttu-id="f28ac-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="f28ac-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBCassandraTable -ResourceGroupName <String> -AccountName <String> -KeyspaceName <String>
 -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-AnalyticalStorageTtl <Int32>] -Schema <PSCassandraSchema> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f28ac-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f28ac-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBCassandraTable -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-TtlInSeconds <Int32>] [-AnalyticalStorageTtl <Int32>] -Schema <PSCassandraSchema>
 -ParentObject <PSCassandraKeyspaceGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f28ac-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f28ac-107">DESCRIPTION</span></span>
<span data-ttu-id="f28ac-108">Erstellt eine neue Tabelle unter "Untere Datenbank".</span><span class="sxs-lookup"><span data-stu-id="f28ac-108">Creates a new CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="f28ac-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f28ac-109">EXAMPLES</span></span>

### <span data-ttu-id="f28ac-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f28ac-110">Example 1</span></span>
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

## <span data-ttu-id="f28ac-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f28ac-111">PARAMETERS</span></span>

### <span data-ttu-id="f28ac-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="f28ac-112">-AccountName</span></span>
<span data-ttu-id="f28ac-113">Name des Dbdatenbankkontos".</span><span class="sxs-lookup"><span data-stu-id="f28ac-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="f28ac-114">-AnalyticalStorageTtl</span><span class="sxs-lookup"><span data-stu-id="f28ac-114">-AnalyticalStorageTtl</span></span>
<span data-ttu-id="f28ac-115">Analytical Storage TTL.</span><span class="sxs-lookup"><span data-stu-id="f28ac-115">Analytical Storage TTL.</span></span>

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

### <span data-ttu-id="f28ac-116">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="f28ac-116">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="f28ac-117">Maximaler Durchsatzwert, wenn die Autoskala aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="f28ac-117">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="f28ac-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f28ac-118">-Confirm</span></span>
<span data-ttu-id="f28ac-119">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f28ac-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f28ac-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f28ac-120">-DefaultProfile</span></span>
<span data-ttu-id="f28ac-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f28ac-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f28ac-122">-KeyspaceName</span><span class="sxs-lookup"><span data-stu-id="f28ac-122">-KeyspaceName</span></span>
<span data-ttu-id="f28ac-123">Name des Tastaturschlüssels.</span><span class="sxs-lookup"><span data-stu-id="f28ac-123">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="f28ac-124">-Name</span><span class="sxs-lookup"><span data-stu-id="f28ac-124">-Name</span></span>
<span data-ttu-id="f28ac-125">DestgensEr Tabellenname.</span><span class="sxs-lookup"><span data-stu-id="f28ac-125">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="f28ac-126">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="f28ac-126">-ParentObject</span></span>
<span data-ttu-id="f28ac-127">Dieses Keyspaceobjekt.</span><span class="sxs-lookup"><span data-stu-id="f28ac-127">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="f28ac-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f28ac-128">-ResourceGroupName</span></span>
<span data-ttu-id="f28ac-129">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="f28ac-129">Name of resource group.</span></span>

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

### <span data-ttu-id="f28ac-130">-Schema</span><span class="sxs-lookup"><span data-stu-id="f28ac-130">-Schema</span></span>
<span data-ttu-id="f28ac-131">PSCasstypSchema-Objekt.</span><span class="sxs-lookup"><span data-stu-id="f28ac-131">PSCassandraSchema object.</span></span>
<span data-ttu-id="f28ac-132">Verwenden sie New-AzCosmosDBCassandraSchema, um dieses Objekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="f28ac-132">Use New-AzCosmosDBCassandraSchema to create this object.</span></span>

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

### <span data-ttu-id="f28ac-133">-Throughput</span><span class="sxs-lookup"><span data-stu-id="f28ac-133">-Throughput</span></span>
<span data-ttu-id="f28ac-134">Der Durchsatz von Keyspace (RU/s).</span><span class="sxs-lookup"><span data-stu-id="f28ac-134">The throughput of Cassandra Keyspace (RU/s).</span></span>
<span data-ttu-id="f28ac-135">Der Standardwert ist 400.</span><span class="sxs-lookup"><span data-stu-id="f28ac-135">Default value is 400.</span></span>

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

### <span data-ttu-id="f28ac-136">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="f28ac-136">-TtlInSeconds</span></span>
<span data-ttu-id="f28ac-137">Standard-Ttl in Sekunden.</span><span class="sxs-lookup"><span data-stu-id="f28ac-137">Default Ttl in seconds.</span></span>
<span data-ttu-id="f28ac-138">Wenn der Wert fehlt oder auf "-1" festgelegt ist, laufen die Elemente nicht ab.</span><span class="sxs-lookup"><span data-stu-id="f28ac-138">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="f28ac-139">Wenn der Wert auf "n" festgelegt ist, laufen die Elemente n Sekunden nach der letzten Änderung ab.</span><span class="sxs-lookup"><span data-stu-id="f28ac-139">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="f28ac-140">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="f28ac-140">-WhatIf</span></span>
<span data-ttu-id="f28ac-141">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f28ac-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f28ac-142">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f28ac-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f28ac-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f28ac-143">CommonParameters</span></span>
<span data-ttu-id="f28ac-144">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f28ac-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f28ac-145">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f28ac-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f28ac-146">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f28ac-146">INPUTS</span></span>

### <span data-ttu-id="f28ac-147">Microsoft.Azure.Commands.DiesDB.Models.PSCassschemaSchema</span><span class="sxs-lookup"><span data-stu-id="f28ac-147">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraSchema</span></span>

### <span data-ttu-id="f28ac-148">Microsoft.Azure.Commands.ExesDB.Models.PSCasskeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="f28ac-148">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="f28ac-149">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f28ac-149">OUTPUTS</span></span>

### <span data-ttu-id="f28ac-150">Microsoft.Azure.Commands.CassDB.Models.PSCassistenTableGetResults</span><span class="sxs-lookup"><span data-stu-id="f28ac-150">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span></span>

### <span data-ttu-id="f28ac-151">Microsoft.Azure.Commands.DiesDB.Exceptions.ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="f28ac-151">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="f28ac-152">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="f28ac-152">NOTES</span></span>

## <span data-ttu-id="f28ac-153">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="f28ac-153">RELATED LINKS</span></span>
