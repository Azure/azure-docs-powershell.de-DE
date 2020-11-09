---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbcassandratablethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraTableThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraTableThroughput.md
ms.openlocfilehash: f686a9923b8281029984a0fc84fcd5d51866256d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94299079"
---
# <span data-ttu-id="b89f9-101">Update-AzCosmosDBCassandraTableThroughput</span><span class="sxs-lookup"><span data-stu-id="b89f9-101">Update-AzCosmosDBCassandraTableThroughput</span></span>

## <span data-ttu-id="b89f9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b89f9-102">SYNOPSIS</span></span>
<span data-ttu-id="b89f9-103">Aktualisiert den Durchsatz einer CosmosDB Cassandra-Tabelle.</span><span class="sxs-lookup"><span data-stu-id="b89f9-103">Updates the throughput value of a CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="b89f9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b89f9-104">SYNTAX</span></span>

### <span data-ttu-id="b89f9-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="b89f9-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBCassandraTableThroughput -KeyspaceName <String> [-Name <String>] -ResourceGroupName <String>
 -AccountName <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b89f9-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b89f9-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraTableThroughput [-Name <String>] -ParentObject <PSCassandraKeyspaceGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b89f9-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b89f9-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraTableThroughput [-Name <String>] -InputObject <PSCassandraTableGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b89f9-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b89f9-108">DESCRIPTION</span></span>
<span data-ttu-id="b89f9-109">Aktualisiert den Durchsatz einer CosmosDB Cassandra-Tabelle.</span><span class="sxs-lookup"><span data-stu-id="b89f9-109">Updates the throughput value of a CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="b89f9-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b89f9-110">EXAMPLES</span></span>

### <span data-ttu-id="b89f9-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b89f9-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBCassandraTableThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -KeyspaceName {myKeyspacename} -Name {myTableName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/cassandraKeyspace/{myKeyspaceName}/tables/{myTableName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="b89f9-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="b89f9-112">PARAMETERS</span></span>

### <span data-ttu-id="b89f9-113">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="b89f9-113">-AccountName</span></span>
<span data-ttu-id="b89f9-114">Name des Cosmos DB-Daten Bankkontos.</span><span class="sxs-lookup"><span data-stu-id="b89f9-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="b89f9-115">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="b89f9-115">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="b89f9-116">Maximaler Durchsatz, wenn "AutoScale" aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="b89f9-116">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="b89f9-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b89f9-117">-Confirm</span></span>
<span data-ttu-id="b89f9-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b89f9-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b89f9-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b89f9-119">-DefaultProfile</span></span>
<span data-ttu-id="b89f9-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b89f9-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b89f9-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="b89f9-121">-InputObject</span></span>
<span data-ttu-id="b89f9-122">Cassandra-Keyspace-Objekt.</span><span class="sxs-lookup"><span data-stu-id="b89f9-122">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="b89f9-123">-Keyspacename</span><span class="sxs-lookup"><span data-stu-id="b89f9-123">-KeyspaceName</span></span>
<span data-ttu-id="b89f9-124">Cassandra-Keyspace-Name.</span><span class="sxs-lookup"><span data-stu-id="b89f9-124">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="b89f9-125">-Name</span><span class="sxs-lookup"><span data-stu-id="b89f9-125">-Name</span></span>
<span data-ttu-id="b89f9-126">Cassandra-Tabellen Name.</span><span class="sxs-lookup"><span data-stu-id="b89f9-126">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="b89f9-127">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="b89f9-127">-ParentObject</span></span>
<span data-ttu-id="b89f9-128">Cassandra-Keyspace-Objekt.</span><span class="sxs-lookup"><span data-stu-id="b89f9-128">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="b89f9-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b89f9-129">-ResourceGroupName</span></span>
<span data-ttu-id="b89f9-130">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="b89f9-130">Name of resource group.</span></span>

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

### <span data-ttu-id="b89f9-131">-Durchsatz</span><span class="sxs-lookup"><span data-stu-id="b89f9-131">-Throughput</span></span>
<span data-ttu-id="b89f9-132">Der Durchsatz des Cassandra-Keyspace (ru/s).</span><span class="sxs-lookup"><span data-stu-id="b89f9-132">The throughput of Cassandra Keyspace (RU/s).</span></span>
<span data-ttu-id="b89f9-133">Der Standardwert ist 400.</span><span class="sxs-lookup"><span data-stu-id="b89f9-133">Default value is 400.</span></span>

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

### <span data-ttu-id="b89f9-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b89f9-134">-WhatIf</span></span>
<span data-ttu-id="b89f9-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b89f9-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b89f9-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b89f9-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b89f9-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b89f9-137">CommonParameters</span></span>
<span data-ttu-id="b89f9-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b89f9-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b89f9-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b89f9-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b89f9-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b89f9-140">INPUTS</span></span>

### <span data-ttu-id="b89f9-141">Microsoft. Azure. Commands. CosmosDB. Models. PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="b89f9-141">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="b89f9-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b89f9-142">OUTPUTS</span></span>

### <span data-ttu-id="b89f9-143">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="b89f9-143">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="b89f9-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="b89f9-144">NOTES</span></span>

## <span data-ttu-id="b89f9-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b89f9-145">RELATED LINKS</span></span>
