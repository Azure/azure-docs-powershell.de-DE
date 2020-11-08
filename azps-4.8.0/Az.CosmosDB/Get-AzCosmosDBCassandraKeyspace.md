---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbcassandrakeyspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraKeyspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraKeyspace.md
ms.openlocfilehash: 30e550ae8670547e6f87ed022053bcbef7927867
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94167101"
---
# <span data-ttu-id="826ac-101">Get-AzCosmosDBCassandraKeyspace</span><span class="sxs-lookup"><span data-stu-id="826ac-101">Get-AzCosmosDBCassandraKeyspace</span></span>

## <span data-ttu-id="826ac-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="826ac-102">SYNOPSIS</span></span>
<span data-ttu-id="826ac-103">Ruft einen CosmosDB Cassandra-Keyspace ab.</span><span class="sxs-lookup"><span data-stu-id="826ac-103">Gets a CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="826ac-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="826ac-104">SYNTAX</span></span>

### <span data-ttu-id="826ac-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="826ac-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBCassandraKeyspace -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="826ac-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="826ac-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBCassandraKeyspace [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="826ac-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="826ac-107">DESCRIPTION</span></span>
<span data-ttu-id="826ac-108">Das Cmdlet " **Get-AzCosmosDBCassandraKeyspace** " erstellt ein neues oder aktualisiert einen vorhandenen CosmosDB Cassandra-Keyspace.</span><span class="sxs-lookup"><span data-stu-id="826ac-108">The **Get-AzCosmosDBCassandraKeyspace** cmdlet creates a new or updates an existing CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="826ac-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="826ac-109">EXAMPLES</span></span>

### <span data-ttu-id="826ac-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="826ac-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBCassandraKeyspace -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Name {name}

Name    Id   Resource
{name}  {id} {resourceObject}
```

<span data-ttu-id="826ac-111">Get-AzCosmosDBCassandraKeyspace ruft die Eigenschaften eines vorhandenen CassandraKeyspace ab.</span><span class="sxs-lookup"><span data-stu-id="826ac-111">Get-AzCosmosDBCassandraKeyspace gets the properties of an existing CassandraKeyspace.</span></span> <span data-ttu-id="826ac-112">Sie können die Ressource erweitern, um die _etag, _ts, _rid Eigenschaften abzurufen.</span><span class="sxs-lookup"><span data-stu-id="826ac-112">You can expand the Resource to get the _etag, _ts, _rid properties.</span></span>

## <span data-ttu-id="826ac-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="826ac-113">PARAMETERS</span></span>

### <span data-ttu-id="826ac-114">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="826ac-114">-AccountName</span></span>
<span data-ttu-id="826ac-115">Name des Cosmos DB-Daten Bankkontos.</span><span class="sxs-lookup"><span data-stu-id="826ac-115">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="826ac-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="826ac-116">-DefaultProfile</span></span>
<span data-ttu-id="826ac-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="826ac-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="826ac-118">-Name</span><span class="sxs-lookup"><span data-stu-id="826ac-118">-Name</span></span>
<span data-ttu-id="826ac-119">Cassandra-Keyspace-Name.</span><span class="sxs-lookup"><span data-stu-id="826ac-119">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="826ac-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="826ac-120">-ParentObject</span></span>
<span data-ttu-id="826ac-121">CosmosDB-Kontoobjekt</span><span class="sxs-lookup"><span data-stu-id="826ac-121">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccountGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="826ac-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="826ac-122">-ResourceGroupName</span></span>
<span data-ttu-id="826ac-123">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="826ac-123">Name of resource group.</span></span>

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

### <span data-ttu-id="826ac-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="826ac-124">CommonParameters</span></span>
<span data-ttu-id="826ac-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="826ac-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="826ac-126">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="826ac-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="826ac-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="826ac-127">INPUTS</span></span>

### <span data-ttu-id="826ac-128">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="826ac-128">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="826ac-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="826ac-129">OUTPUTS</span></span>

### <span data-ttu-id="826ac-130">Microsoft. Azure. Commands. CosmosDB. Models. PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="826ac-130">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

### <span data-ttu-id="826ac-131">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="826ac-131">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="826ac-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="826ac-132">NOTES</span></span>

## <span data-ttu-id="826ac-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="826ac-133">RELATED LINKS</span></span>
