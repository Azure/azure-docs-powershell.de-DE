---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbcassandrakeyspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraKeyspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraKeyspace.md
ms.openlocfilehash: cd9c9ba5f46ec83cf9b804e103ad1038662ca271
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93845640"
---
# <span data-ttu-id="0fdd0-101">Get-AzCosmosDBCassandraKeyspace</span><span class="sxs-lookup"><span data-stu-id="0fdd0-101">Get-AzCosmosDBCassandraKeyspace</span></span>

## <span data-ttu-id="0fdd0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0fdd0-102">SYNOPSIS</span></span>
<span data-ttu-id="0fdd0-103">Ruft einen CosmosDB Cassandra-Keyspace ab.</span><span class="sxs-lookup"><span data-stu-id="0fdd0-103">Gets a CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="0fdd0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0fdd0-104">SYNTAX</span></span>

### <span data-ttu-id="0fdd0-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="0fdd0-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBCassandraKeyspace -ResourceGroupName <String> -AccountName <String> [-Name <String>] [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0fdd0-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0fdd0-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBCassandraKeyspace [-Name <String>] -InputObject <PSDatabaseAccount> [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0fdd0-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0fdd0-107">DESCRIPTION</span></span>
<span data-ttu-id="0fdd0-108">Das Cmdlet " **Get-AzCosmosDBCassandraKeyspace** " erstellt ein neues oder aktualisiert einen vorhandenen CosmosDB Cassandra-Keyspace.</span><span class="sxs-lookup"><span data-stu-id="0fdd0-108">The **Get-AzCosmosDBCassandraKeyspace** cmdlet creates a new or updates an existing CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="0fdd0-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0fdd0-109">EXAMPLES</span></span>

### <span data-ttu-id="0fdd0-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0fdd0-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBCassandraKeyspace -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Name {name}

Name    Id   Resource
{name}  {id} {resourceObject}
```

<span data-ttu-id="0fdd0-111">Get-AzCosmosDBCassandraKeyspace ruft die Eigenschaften eines vorhandenen CassandraKeyspace ab.</span><span class="sxs-lookup"><span data-stu-id="0fdd0-111">Get-AzCosmosDBCassandraKeyspace gets the properties of an existing CassandraKeyspace.</span></span> <span data-ttu-id="0fdd0-112">Sie können die Ressource erweitern, um die _etag, _ts, _rid Eigenschaften abzurufen.</span><span class="sxs-lookup"><span data-stu-id="0fdd0-112">You can expand the Resource to get the _etag, _ts, _rid properties.</span></span>

## <span data-ttu-id="0fdd0-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="0fdd0-113">PARAMETERS</span></span>

### <span data-ttu-id="0fdd0-114">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="0fdd0-114">-AccountName</span></span>
<span data-ttu-id="0fdd0-115">Name des Cosmos DB-Daten Bankkontos.</span><span class="sxs-lookup"><span data-stu-id="0fdd0-115">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="0fdd0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0fdd0-116">-DefaultProfile</span></span>
<span data-ttu-id="0fdd0-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0fdd0-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0fdd0-118">-Detailliert</span><span class="sxs-lookup"><span data-stu-id="0fdd0-118">-Detailed</span></span>
<span data-ttu-id="0fdd0-119">Wenn Sie dann bereitgestellt werden, gibt das Cmdlet den Keyspace mit dem entsprechenden Durchsatz zurück.</span><span class="sxs-lookup"><span data-stu-id="0fdd0-119">If provided then, the cmdlet returns the Keyspace with the corresponding throughput value.</span></span>

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

### <span data-ttu-id="0fdd0-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="0fdd0-120">-InputObject</span></span>
<span data-ttu-id="0fdd0-121">CosmosDB-Kontoobjekt</span><span class="sxs-lookup"><span data-stu-id="0fdd0-121">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0fdd0-122">-Name</span><span class="sxs-lookup"><span data-stu-id="0fdd0-122">-Name</span></span>
<span data-ttu-id="0fdd0-123">Cassandra-Keyspace-Name.</span><span class="sxs-lookup"><span data-stu-id="0fdd0-123">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="0fdd0-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0fdd0-124">-ResourceGroupName</span></span>
<span data-ttu-id="0fdd0-125">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="0fdd0-125">Name of resource group.</span></span>

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

### <span data-ttu-id="0fdd0-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fdd0-126">CommonParameters</span></span>
<span data-ttu-id="0fdd0-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0fdd0-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0fdd0-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0fdd0-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fdd0-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0fdd0-129">INPUTS</span></span>

### <span data-ttu-id="0fdd0-130">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="0fdd0-130">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="0fdd0-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0fdd0-131">OUTPUTS</span></span>

### <span data-ttu-id="0fdd0-132">Microsoft. Azure. Commands. CosmosDB. Models. PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="0fdd0-132">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

### <span data-ttu-id="0fdd0-133">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="0fdd0-133">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="0fdd0-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="0fdd0-134">NOTES</span></span>

## <span data-ttu-id="0fdd0-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0fdd0-135">RELATED LINKS</span></span>
