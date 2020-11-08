---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/set-azcosmosdbcassandratable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBCassandraTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBCassandraTable.md
ms.openlocfilehash: e79353d5265a2d58b72e49ee1978ea92599bed39
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94004645"
---
# <span data-ttu-id="99f02-101">Set-AzCosmosDBCassandraTable</span><span class="sxs-lookup"><span data-stu-id="99f02-101">Set-AzCosmosDBCassandraTable</span></span>

## <span data-ttu-id="99f02-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="99f02-102">SYNOPSIS</span></span>
<span data-ttu-id="99f02-103">Legt die CosmosDB Cassandra-Tabelle fest.</span><span class="sxs-lookup"><span data-stu-id="99f02-103">Sets the CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="99f02-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="99f02-104">SYNTAX</span></span>

### <span data-ttu-id="99f02-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="99f02-105">ByNameParameterSet (Default)</span></span>
```
Set-AzCosmosDBCassandraTable -ResourceGroupName <String> -AccountName <String> -KeyspaceName <String>
 -Name <String> [-Throughput <Int32>] [-TtlInSeconds <Int32>] -Schema <PSCassandraSchema>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="99f02-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="99f02-106">ByParentObjectParameterSet</span></span>
```
Set-AzCosmosDBCassandraTable -Name <String> [-Throughput <Int32>] [-TtlInSeconds <Int32>]
 -Schema <PSCassandraSchema> -InputObject <PSCassandraKeyspaceGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="99f02-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="99f02-107">DESCRIPTION</span></span>
<span data-ttu-id="99f02-108">Das Cmdlet " **Set-AzCosmosDBCassandraTable** " legt den CosmosDB-Cassandra-Keyspace fest.</span><span class="sxs-lookup"><span data-stu-id="99f02-108">The **Set-AzCosmosDBCassandraTable** cmdlet sets the CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="99f02-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="99f02-109">EXAMPLES</span></span>

### <span data-ttu-id="99f02-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="99f02-110">Example 1</span></span>
```powershell
PS C:\> Set-AzCosmosDBCassandraTable -ResourceGroupName {rgName} -AccountName {accountName} -Keyspace {keyspaceName} -Name {tableName}
Name        Id    Resource
----        --    -------
{name}     {id}   Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetPropertiesResource
```

<span data-ttu-id="99f02-111">Das Resource-Objekt enthält die Werte der _rid-, _ts-, _etag-, DefaultTtl-und Schema Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="99f02-111">Resource object contains the values of the _rid, _ts, _etag, DefaultTtl and Schema properties.</span></span>

## <span data-ttu-id="99f02-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="99f02-112">PARAMETERS</span></span>

### <span data-ttu-id="99f02-113">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="99f02-113">-AccountName</span></span>
<span data-ttu-id="99f02-114">Name des Cosmos DB-Daten Bankkontos.</span><span class="sxs-lookup"><span data-stu-id="99f02-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="99f02-115">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="99f02-115">-Confirm</span></span>
<span data-ttu-id="99f02-116">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="99f02-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="99f02-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99f02-117">-DefaultProfile</span></span>
<span data-ttu-id="99f02-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="99f02-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="99f02-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="99f02-119">-InputObject</span></span>
<span data-ttu-id="99f02-120">Cassandra-Keyspace-Objekt.</span><span class="sxs-lookup"><span data-stu-id="99f02-120">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="99f02-121">-Keyspacename</span><span class="sxs-lookup"><span data-stu-id="99f02-121">-KeyspaceName</span></span>
<span data-ttu-id="99f02-122">Cassandra-Keyspace-Name.</span><span class="sxs-lookup"><span data-stu-id="99f02-122">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="99f02-123">-Name</span><span class="sxs-lookup"><span data-stu-id="99f02-123">-Name</span></span>
<span data-ttu-id="99f02-124">Cassandra-Tabellen Name.</span><span class="sxs-lookup"><span data-stu-id="99f02-124">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="99f02-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99f02-125">-ResourceGroupName</span></span>
<span data-ttu-id="99f02-126">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="99f02-126">Name of resource group.</span></span>

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

### <span data-ttu-id="99f02-127">-Schema</span><span class="sxs-lookup"><span data-stu-id="99f02-127">-Schema</span></span>
<span data-ttu-id="99f02-128">PSCassandraSchema-Objekt.</span><span class="sxs-lookup"><span data-stu-id="99f02-128">PSCassandraSchema object.</span></span>
<span data-ttu-id="99f02-129">Verwenden Sie New-AzCosmosDBCassandraSchema, um dieses Objekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="99f02-129">Use New-AzCosmosDBCassandraSchema to create this object.</span></span>

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

### <span data-ttu-id="99f02-130">-Durchsatz</span><span class="sxs-lookup"><span data-stu-id="99f02-130">-Throughput</span></span>
<span data-ttu-id="99f02-131">Der Durchsatz des Cassandra-Keyspace (ru/s).</span><span class="sxs-lookup"><span data-stu-id="99f02-131">The throughput of Cassandra Keyspace (RU/s).</span></span>
<span data-ttu-id="99f02-132">Der Standardwert ist 400.</span><span class="sxs-lookup"><span data-stu-id="99f02-132">Default value is 400.</span></span>

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

### <span data-ttu-id="99f02-133">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="99f02-133">-TtlInSeconds</span></span>
<span data-ttu-id="99f02-134">Standard-TTL in Sekunden.</span><span class="sxs-lookup"><span data-stu-id="99f02-134">Default Ttl in seconds.</span></span>
<span data-ttu-id="99f02-135">Wenn der Wert fehlt oder auf-1 gesetzt ist, werden die Elemente nicht ablaufen.</span><span class="sxs-lookup"><span data-stu-id="99f02-135">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="99f02-136">Wenn der Wert auf n gesetzt ist, werden die Elemente nach dem Zeitpunkt der letzten Änderung n Sekunden ablaufen.</span><span class="sxs-lookup"><span data-stu-id="99f02-136">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="99f02-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99f02-137">-WhatIf</span></span>
<span data-ttu-id="99f02-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="99f02-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="99f02-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="99f02-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="99f02-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99f02-140">CommonParameters</span></span>
<span data-ttu-id="99f02-141">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99f02-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99f02-142">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="99f02-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99f02-143">Eingaben</span><span class="sxs-lookup"><span data-stu-id="99f02-143">INPUTS</span></span>

### <span data-ttu-id="99f02-144">Microsoft. Azure. Commands. CosmosDB. Models. PSCassandraSchema</span><span class="sxs-lookup"><span data-stu-id="99f02-144">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraSchema</span></span>

### <span data-ttu-id="99f02-145">Microsoft. Azure. Commands. CosmosDB. Models. PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="99f02-145">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="99f02-146">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="99f02-146">OUTPUTS</span></span>

### <span data-ttu-id="99f02-147">Microsoft. Azure. Commands. CosmosDB. Models. PSCassandraTableGetResults</span><span class="sxs-lookup"><span data-stu-id="99f02-147">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span></span>

## <span data-ttu-id="99f02-148">Notizen</span><span class="sxs-lookup"><span data-stu-id="99f02-148">NOTES</span></span>

## <span data-ttu-id="99f02-149">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="99f02-149">RELATED LINKS</span></span>
