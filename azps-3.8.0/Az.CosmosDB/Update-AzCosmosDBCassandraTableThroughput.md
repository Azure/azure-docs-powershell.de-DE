---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbcassandratablethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraTableThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraTableThroughput.md
ms.openlocfilehash: 9c3aff7edb26863f2843ef517c7ce0f08f91296f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94004629"
---
# <span data-ttu-id="4581e-101">Update-AzCosmosDBCassandraTableThroughput</span><span class="sxs-lookup"><span data-stu-id="4581e-101">Update-AzCosmosDBCassandraTableThroughput</span></span>

## <span data-ttu-id="4581e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4581e-102">SYNOPSIS</span></span>
<span data-ttu-id="4581e-103">Aktualisiert den Durchsatz einer CosmosDB Cassandra-Tabelle.</span><span class="sxs-lookup"><span data-stu-id="4581e-103">Updates the throughput value of a CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="4581e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4581e-104">SYNTAX</span></span>

### <span data-ttu-id="4581e-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="4581e-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBCassandraTableThroughput -ResourceGroupName <String> -AccountName <String>
 -KeyspaceName <String> [-Name <String>] -Throughput <Int32> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4581e-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4581e-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraTableThroughput [-Name <String>] -Throughput <Int32>
 -ParentObject <PSCassandraKeyspaceGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4581e-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4581e-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraTableThroughput [-Name <String>] -Throughput <Int32>
 -InputObject <PSCassandraTableGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4581e-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4581e-108">EXAMPLES</span></span>

### <span data-ttu-id="4581e-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4581e-109">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBCassandraTableThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -KeyspaceName {myKeyspacename} -Name {myTableName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/cassandraKeyspace/{myKeyspaceName}/tables/{myTableName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="4581e-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="4581e-110">PARAMETERS</span></span>

### <span data-ttu-id="4581e-111">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="4581e-111">-AccountName</span></span>
<span data-ttu-id="4581e-112">Name des Cosmos DB-Daten Bankkontos.</span><span class="sxs-lookup"><span data-stu-id="4581e-112">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="4581e-113">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4581e-113">-Confirm</span></span>
<span data-ttu-id="4581e-114">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4581e-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4581e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4581e-115">-DefaultProfile</span></span>
<span data-ttu-id="4581e-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4581e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4581e-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="4581e-117">-InputObject</span></span>
<span data-ttu-id="4581e-118">Cassandra-Keyspace-Objekt.</span><span class="sxs-lookup"><span data-stu-id="4581e-118">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="4581e-119">-Keyspacename</span><span class="sxs-lookup"><span data-stu-id="4581e-119">-KeyspaceName</span></span>
<span data-ttu-id="4581e-120">Cassandra-Keyspace-Name.</span><span class="sxs-lookup"><span data-stu-id="4581e-120">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="4581e-121">-Name</span><span class="sxs-lookup"><span data-stu-id="4581e-121">-Name</span></span>
<span data-ttu-id="4581e-122">Cassandra-Tabellen Name.</span><span class="sxs-lookup"><span data-stu-id="4581e-122">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="4581e-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="4581e-123">-ParentObject</span></span>
<span data-ttu-id="4581e-124">Cassandra-Keyspace-Objekt.</span><span class="sxs-lookup"><span data-stu-id="4581e-124">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="4581e-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4581e-125">-ResourceGroupName</span></span>
<span data-ttu-id="4581e-126">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="4581e-126">Name of resource group.</span></span>

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

### <span data-ttu-id="4581e-127">-Durchsatz</span><span class="sxs-lookup"><span data-stu-id="4581e-127">-Throughput</span></span>
<span data-ttu-id="4581e-128">Der Durchsatz des Cassandra-Keyspace (ru/s).</span><span class="sxs-lookup"><span data-stu-id="4581e-128">The throughput of Cassandra Keyspace (RU/s).</span></span>
<span data-ttu-id="4581e-129">Der Standardwert ist 400.</span><span class="sxs-lookup"><span data-stu-id="4581e-129">Default value is 400.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4581e-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4581e-130">-WhatIf</span></span>
<span data-ttu-id="4581e-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4581e-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4581e-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4581e-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4581e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4581e-133">CommonParameters</span></span>
<span data-ttu-id="4581e-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4581e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4581e-135">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4581e-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4581e-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4581e-136">INPUTS</span></span>

### <span data-ttu-id="4581e-137">Microsoft. Azure. Commands. CosmosDB. Models. PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="4581e-137">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="4581e-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4581e-138">OUTPUTS</span></span>

### <span data-ttu-id="4581e-139">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="4581e-139">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="4581e-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="4581e-140">NOTES</span></span>

## <span data-ttu-id="4581e-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4581e-141">RELATED LINKS</span></span>
