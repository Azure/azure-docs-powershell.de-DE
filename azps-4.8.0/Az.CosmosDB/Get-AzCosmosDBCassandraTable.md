---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbcassandratable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraTable.md
ms.openlocfilehash: 8994cab45a10f874d0c544f231e20c27a01039f4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94175301"
---
# <span data-ttu-id="d624a-101">Get-AzCosmosDBCassandraTable</span><span class="sxs-lookup"><span data-stu-id="d624a-101">Get-AzCosmosDBCassandraTable</span></span>

## <span data-ttu-id="d624a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d624a-102">SYNOPSIS</span></span>
<span data-ttu-id="d624a-103">Ruft eine CosmosDB Cassandra-Tabelle ab.</span><span class="sxs-lookup"><span data-stu-id="d624a-103">Gets a CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="d624a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d624a-104">SYNTAX</span></span>

### <span data-ttu-id="d624a-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="d624a-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBCassandraTable -AccountName <String> -KeyspaceName <String> -ResourceGroupName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d624a-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d624a-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBCassandraTable [-Name <String>] -ParentObject <PSCassandraKeyspaceGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d624a-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d624a-107">DESCRIPTION</span></span>
<span data-ttu-id="d624a-108">Das Cmdlet " **Get-AzCosmosDBCassandraTable** " erstellt ein neues oder aktualisiert einen vorhandenen CosmosDB Cassandra-Keyspace.</span><span class="sxs-lookup"><span data-stu-id="d624a-108">The **Get-AzCosmosDBCassandraTable** cmdlet creates a new or updates an existing CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="d624a-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d624a-109">EXAMPLES</span></span>

### <span data-ttu-id="d624a-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d624a-110">Example 1</span></span>
```powershell
PS C:\> $table = Get-AzCosmosDBCassandraTable -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Keyspace {keyspaceName} -Name {name}

Name    Id   Resource
{name}  {id} {resourceObject}
```

<span data-ttu-id="d624a-111">{{Get-AzCosmosDBCassandraTable ruft die Eigenschaften eines vorhandenen CassandraKeyspace ab.</span><span class="sxs-lookup"><span data-stu-id="d624a-111">{{ Get-AzCosmosDBCassandraTable gets the properties of an existing CassandraKeyspace.</span></span> <span data-ttu-id="d624a-112">Sie können die Ressource erweitern, um die DefaultTtl-, Schema-, _etag-, _ts-_rid-Eigenschaften abzurufen.}}</span><span class="sxs-lookup"><span data-stu-id="d624a-112">You can expand the Resource to get the DefaultTtl, Schema, _etag, _ts, _rid properties.}}</span></span>

## <span data-ttu-id="d624a-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="d624a-113">PARAMETERS</span></span>

### <span data-ttu-id="d624a-114">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="d624a-114">-AccountName</span></span>
<span data-ttu-id="d624a-115">Name des Cosmos DB-Daten Bankkontos.</span><span class="sxs-lookup"><span data-stu-id="d624a-115">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="d624a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d624a-116">-DefaultProfile</span></span>
<span data-ttu-id="d624a-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d624a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d624a-118">-Keyspacename</span><span class="sxs-lookup"><span data-stu-id="d624a-118">-KeyspaceName</span></span>
<span data-ttu-id="d624a-119">Cassandra-Keyspace-Name.</span><span class="sxs-lookup"><span data-stu-id="d624a-119">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="d624a-120">-Name</span><span class="sxs-lookup"><span data-stu-id="d624a-120">-Name</span></span>
<span data-ttu-id="d624a-121">Cassandra-Tabellen Name.</span><span class="sxs-lookup"><span data-stu-id="d624a-121">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="d624a-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="d624a-122">-ParentObject</span></span>
<span data-ttu-id="d624a-123">Cassandra-Keyspace-Objekt.</span><span class="sxs-lookup"><span data-stu-id="d624a-123">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="d624a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d624a-124">-ResourceGroupName</span></span>
<span data-ttu-id="d624a-125">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="d624a-125">Name of resource group.</span></span>

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

### <span data-ttu-id="d624a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d624a-126">CommonParameters</span></span>
<span data-ttu-id="d624a-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d624a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d624a-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d624a-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d624a-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d624a-129">INPUTS</span></span>

### <span data-ttu-id="d624a-130">Microsoft. Azure. Commands. CosmosDB. Models. PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="d624a-130">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="d624a-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d624a-131">OUTPUTS</span></span>

### <span data-ttu-id="d624a-132">Microsoft. Azure. Commands. CosmosDB. Models. PSCassandraTableGetResults</span><span class="sxs-lookup"><span data-stu-id="d624a-132">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span></span>

### <span data-ttu-id="d624a-133">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="d624a-133">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="d624a-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="d624a-134">NOTES</span></span>

## <span data-ttu-id="d624a-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d624a-135">RELATED LINKS</span></span>
