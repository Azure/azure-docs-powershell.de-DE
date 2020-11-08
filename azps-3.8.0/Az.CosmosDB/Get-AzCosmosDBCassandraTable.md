---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbcassandratable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraTable.md
ms.openlocfilehash: ca78194e0e47b07d2d0d061829bf4db38d85632a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94004333"
---
# <span data-ttu-id="428c2-101">Get-AzCosmosDBCassandraTable</span><span class="sxs-lookup"><span data-stu-id="428c2-101">Get-AzCosmosDBCassandraTable</span></span>

## <span data-ttu-id="428c2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="428c2-102">SYNOPSIS</span></span>
<span data-ttu-id="428c2-103">Ruft eine CosmosDB Cassandra-Tabelle ab.</span><span class="sxs-lookup"><span data-stu-id="428c2-103">Gets a CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="428c2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="428c2-104">SYNTAX</span></span>

### <span data-ttu-id="428c2-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="428c2-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBCassandraTable -AccountName <String> -KeyspaceName <String> -ResourceGroupName <String>
 [-Name <String>] [-Detailed] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="428c2-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="428c2-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBCassandraTable [-Name <String>] -InputObject <PSCassandraKeyspaceGetResults> [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="428c2-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="428c2-107">DESCRIPTION</span></span>
<span data-ttu-id="428c2-108">Das Cmdlet " **Get-AzCosmosDBCassandraTable** " erstellt ein neues oder aktualisiert einen vorhandenen CosmosDB Cassandra-Keyspace.</span><span class="sxs-lookup"><span data-stu-id="428c2-108">The **Get-AzCosmosDBCassandraTable** cmdlet creates a new or updates an existing CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="428c2-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="428c2-109">EXAMPLES</span></span>

### <span data-ttu-id="428c2-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="428c2-110">Example 1</span></span>
```powershell
PS C:\> $table = Get-AzCosmosDBCassandraTable -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Keyspace {keyspaceName} -Name {name}

Name    Id   Resource
{name}  {id} {resourceObject}
```

<span data-ttu-id="428c2-111">{{Get-AzCosmosDBCassandraTable ruft die Eigenschaften eines vorhandenen CassandraKeyspace ab.</span><span class="sxs-lookup"><span data-stu-id="428c2-111">{{ Get-AzCosmosDBCassandraTable gets the properties of an existing CassandraKeyspace.</span></span> <span data-ttu-id="428c2-112">Sie können die Ressource erweitern, um die DefaultTtl-, Schema-, _etag-, _ts-_rid-Eigenschaften abzurufen.}}</span><span class="sxs-lookup"><span data-stu-id="428c2-112">You can expand the Resource to get the DefaultTtl, Schema, _etag, _ts, _rid properties.}}</span></span>

## <span data-ttu-id="428c2-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="428c2-113">PARAMETERS</span></span>

### <span data-ttu-id="428c2-114">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="428c2-114">-AccountName</span></span>
<span data-ttu-id="428c2-115">Name des Cosmos DB-Daten Bankkontos.</span><span class="sxs-lookup"><span data-stu-id="428c2-115">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="428c2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="428c2-116">-DefaultProfile</span></span>
<span data-ttu-id="428c2-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="428c2-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="428c2-118">-Detailliert</span><span class="sxs-lookup"><span data-stu-id="428c2-118">-Detailed</span></span>
<span data-ttu-id="428c2-119">Wenn Sie dann bereitgestellt werden, gibt das Cmdlet die Cassandra-Tabelle mit dem entsprechenden Durchsatz zurück.</span><span class="sxs-lookup"><span data-stu-id="428c2-119">If provided then, the cmdlet returns the Cassandra Table with the corresponding throughput value.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="428c2-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="428c2-120">-InputObject</span></span>
<span data-ttu-id="428c2-121">Cassandra-Keyspace-Objekt.</span><span class="sxs-lookup"><span data-stu-id="428c2-121">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="428c2-122">-Keyspacename</span><span class="sxs-lookup"><span data-stu-id="428c2-122">-KeyspaceName</span></span>
<span data-ttu-id="428c2-123">Cassandra-Keyspace-Name.</span><span class="sxs-lookup"><span data-stu-id="428c2-123">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="428c2-124">-Name</span><span class="sxs-lookup"><span data-stu-id="428c2-124">-Name</span></span>
<span data-ttu-id="428c2-125">Cassandra-Tabellen Name.</span><span class="sxs-lookup"><span data-stu-id="428c2-125">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="428c2-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="428c2-126">-ResourceGroupName</span></span>
<span data-ttu-id="428c2-127">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="428c2-127">Name of resource group.</span></span>

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

### <span data-ttu-id="428c2-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="428c2-128">CommonParameters</span></span>
<span data-ttu-id="428c2-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="428c2-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="428c2-130">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="428c2-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="428c2-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="428c2-131">INPUTS</span></span>

### <span data-ttu-id="428c2-132">Microsoft. Azure. Commands. CosmosDB. Models. PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="428c2-132">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="428c2-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="428c2-133">OUTPUTS</span></span>

### <span data-ttu-id="428c2-134">Microsoft. Azure. Commands. CosmosDB. Models. PSCassandraTableGetResults</span><span class="sxs-lookup"><span data-stu-id="428c2-134">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span></span>

### <span data-ttu-id="428c2-135">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="428c2-135">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="428c2-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="428c2-136">NOTES</span></span>

## <span data-ttu-id="428c2-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="428c2-137">RELATED LINKS</span></span>
