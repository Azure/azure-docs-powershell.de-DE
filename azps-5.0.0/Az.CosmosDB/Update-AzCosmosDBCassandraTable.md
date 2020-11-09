---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbcassandratable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraTable.md
ms.openlocfilehash: 6fad5017dbd7dd258e44e69638a919e53597ec9d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94299074"
---
# <span data-ttu-id="34981-101">Update-AzCosmosDBCassandraTable</span><span class="sxs-lookup"><span data-stu-id="34981-101">Update-AzCosmosDBCassandraTable</span></span>

## <span data-ttu-id="34981-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="34981-102">SYNOPSIS</span></span>
<span data-ttu-id="34981-103">Aktualisiert die CosmosDB Cassandra-Tabelle.</span><span class="sxs-lookup"><span data-stu-id="34981-103">Updates the CosmosDB Cassandra Table.</span></span> <span data-ttu-id="34981-104">Führt einen clientseitigen Patch-Vorgang durchlesen der vorhandenen Tabelle aus.</span><span class="sxs-lookup"><span data-stu-id="34981-104">Performs a client side patch operation by reading the existing Table.</span></span>

## <span data-ttu-id="34981-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="34981-105">SYNTAX</span></span>

### <span data-ttu-id="34981-106">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="34981-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBCassandraTable -ResourceGroupName <String> -AccountName <String> -KeyspaceName <String>
 [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-AnalyticalStorageTtl <Int32>] [-Schema <PSCassandraSchema>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34981-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="34981-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraTable [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-TtlInSeconds <Int32>] [-AnalyticalStorageTtl <Int32>] [-Schema <PSCassandraSchema>]
 -ParentObject <PSCassandraKeyspaceGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="34981-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="34981-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraTable [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-TtlInSeconds <Int32>] [-AnalyticalStorageTtl <Int32>] [-Schema <PSCassandraSchema>]
 -InputObject <PSCassandraTableGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="34981-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="34981-109">DESCRIPTION</span></span>
<span data-ttu-id="34981-110">Aktualisiert die CosmosDB Cassandra-Tabelle.</span><span class="sxs-lookup"><span data-stu-id="34981-110">Updates the CosmosDB Cassandra Table.</span></span> <span data-ttu-id="34981-111">Führt einen clientseitigen Patch-Vorgang durchlesen der vorhandenen Tabelle aus.</span><span class="sxs-lookup"><span data-stu-id="34981-111">Performs a client side patch operation by reading the existing Table.</span></span>

## <span data-ttu-id="34981-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="34981-112">EXAMPLES</span></span>

### <span data-ttu-id="34981-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="34981-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBCassandraTable -AccountName myAccountName -ResourceGroupName myRgName -KeyspaceName myKeyspaceName -Name myTableName -Schema updatedSchema
        Name     : myTable
        Id       : /subscriptions/mySubId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/cassandraKeyspaces/myKeyspaceName/t
                ables/myTableName
        Location :
        Tags     :
        Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetPropertiesResource
```

<span data-ttu-id="34981-114">{{Add Example Description here}}</span><span class="sxs-lookup"><span data-stu-id="34981-114">{{ Add example description here }}</span></span>

## <span data-ttu-id="34981-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="34981-115">PARAMETERS</span></span>

### <span data-ttu-id="34981-116">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="34981-116">-AccountName</span></span>
<span data-ttu-id="34981-117">Name des Cosmos DB-Daten Bankkontos.</span><span class="sxs-lookup"><span data-stu-id="34981-117">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="34981-118">-AnalyticalStorageTtl</span><span class="sxs-lookup"><span data-stu-id="34981-118">-AnalyticalStorageTtl</span></span>
<span data-ttu-id="34981-119">Analytische Speicher TTL.</span><span class="sxs-lookup"><span data-stu-id="34981-119">Analytical Storage TTL.</span></span>

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

### <span data-ttu-id="34981-120">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="34981-120">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="34981-121">Maximaler Durchsatz, wenn "AutoScale" aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="34981-121">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="34981-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="34981-122">-Confirm</span></span>
<span data-ttu-id="34981-123">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="34981-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34981-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34981-124">-DefaultProfile</span></span>
<span data-ttu-id="34981-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="34981-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="34981-126">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="34981-126">-InputObject</span></span>
<span data-ttu-id="34981-127">Cassandra-Tabellenobjekt.</span><span class="sxs-lookup"><span data-stu-id="34981-127">Cassandra Table object.</span></span>

```yaml
Type: PSCassandraTableGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="34981-128">-Keyspacename</span><span class="sxs-lookup"><span data-stu-id="34981-128">-KeyspaceName</span></span>
<span data-ttu-id="34981-129">Cassandra-Keyspace-Name.</span><span class="sxs-lookup"><span data-stu-id="34981-129">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="34981-130">-Name</span><span class="sxs-lookup"><span data-stu-id="34981-130">-Name</span></span>
<span data-ttu-id="34981-131">Cassandra-Tabellen Name.</span><span class="sxs-lookup"><span data-stu-id="34981-131">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="34981-132">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="34981-132">-ParentObject</span></span>
<span data-ttu-id="34981-133">Cassandra-Keyspace-Objekt.</span><span class="sxs-lookup"><span data-stu-id="34981-133">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="34981-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34981-134">-ResourceGroupName</span></span>
<span data-ttu-id="34981-135">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="34981-135">Name of resource group.</span></span>

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

### <span data-ttu-id="34981-136">-Schema</span><span class="sxs-lookup"><span data-stu-id="34981-136">-Schema</span></span>
<span data-ttu-id="34981-137">PSCassandraSchema-Objekt.</span><span class="sxs-lookup"><span data-stu-id="34981-137">PSCassandraSchema object.</span></span>
<span data-ttu-id="34981-138">Verwenden Sie New-AzCosmosDBCassandraSchema, um dieses Objekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="34981-138">Use New-AzCosmosDBCassandraSchema to create this object.</span></span>

```yaml
Type: PSCassandraSchema
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="34981-139">-Durchsatz</span><span class="sxs-lookup"><span data-stu-id="34981-139">-Throughput</span></span>
<span data-ttu-id="34981-140">Der Durchsatz des Cassandra-Keyspace (ru/s).</span><span class="sxs-lookup"><span data-stu-id="34981-140">The throughput of Cassandra Keyspace (RU/s).</span></span>
<span data-ttu-id="34981-141">Der Standardwert ist 400.</span><span class="sxs-lookup"><span data-stu-id="34981-141">Default value is 400.</span></span>

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

### <span data-ttu-id="34981-142">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="34981-142">-TtlInSeconds</span></span>
<span data-ttu-id="34981-143">Standard-TTL in Sekunden.</span><span class="sxs-lookup"><span data-stu-id="34981-143">Default Ttl in seconds.</span></span>
<span data-ttu-id="34981-144">Wenn der Wert fehlt oder auf-1 gesetzt ist, werden die Elemente nicht ablaufen.</span><span class="sxs-lookup"><span data-stu-id="34981-144">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="34981-145">Wenn der Wert auf n gesetzt ist, werden die Elemente nach dem Zeitpunkt der letzten Änderung n Sekunden ablaufen.</span><span class="sxs-lookup"><span data-stu-id="34981-145">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="34981-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34981-146">-WhatIf</span></span>
<span data-ttu-id="34981-147">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="34981-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="34981-148">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="34981-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="34981-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34981-149">CommonParameters</span></span>
<span data-ttu-id="34981-150">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34981-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34981-151">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="34981-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34981-152">Eingaben</span><span class="sxs-lookup"><span data-stu-id="34981-152">INPUTS</span></span>

### <span data-ttu-id="34981-153">Microsoft. Azure. Commands. CosmosDB. Models. PSCassandraSchema</span><span class="sxs-lookup"><span data-stu-id="34981-153">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraSchema</span></span>

### <span data-ttu-id="34981-154">Microsoft. Azure. Commands. CosmosDB. Models. PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="34981-154">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

### <span data-ttu-id="34981-155">Microsoft. Azure. Commands. CosmosDB. Models. PSCassandraTableGetResults</span><span class="sxs-lookup"><span data-stu-id="34981-155">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span></span>

## <span data-ttu-id="34981-156">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="34981-156">OUTPUTS</span></span>

### <span data-ttu-id="34981-157">Microsoft. Azure. Commands. CosmosDB. Models. PSCassandraTableGetResults</span><span class="sxs-lookup"><span data-stu-id="34981-157">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span></span>

### <span data-ttu-id="34981-158">Microsoft. Azure. Commands. CosmosDB. Exceptions. ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="34981-158">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="34981-159">Notizen</span><span class="sxs-lookup"><span data-stu-id="34981-159">NOTES</span></span>

## <span data-ttu-id="34981-160">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="34981-160">RELATED LINKS</span></span>
