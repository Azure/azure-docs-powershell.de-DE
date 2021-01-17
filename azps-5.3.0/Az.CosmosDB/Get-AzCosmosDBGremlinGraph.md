---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbgremlingraph
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinGraph.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinGraph.md
ms.openlocfilehash: 1b8bcbdeb797aea0faa5e9b3a0b5cb1e36b0f1b9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98472858"
---
# <span data-ttu-id="4e929-101">Get-AzCosmosDBGremlinGraph</span><span class="sxs-lookup"><span data-stu-id="4e929-101">Get-AzCosmosDBGremlinGraph</span></span>

## <span data-ttu-id="4e929-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4e929-102">SYNOPSIS</span></span>
<span data-ttu-id="4e929-103">Ruft das Grafische Diagramm des Unternesdb-Gremlin Graph ab.</span><span class="sxs-lookup"><span data-stu-id="4e929-103">Gets the CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="4e929-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4e929-104">SYNTAX</span></span>

### <span data-ttu-id="4e929-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="4e929-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBGremlinGraph -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] -AccountName <String> -DatabaseName <String> [<CommonParameters>]
```

### <span data-ttu-id="4e929-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4e929-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBGremlinGraph [-Name <String>] -ParentObject <PSGremlinDatabaseGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4e929-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4e929-107">DESCRIPTION</span></span>
<span data-ttu-id="4e929-108">Das **Cmdlet "Get-AzCosmosDBGremlinGraph"** ruft die Eigenschaften von "DessDB Gremlin Graph" ab.</span><span class="sxs-lookup"><span data-stu-id="4e929-108">The **Get-AzCosmosDBGremlinGraph** cmdlet gets the CosmosDB Gremlin Graph properties.</span></span>

## <span data-ttu-id="4e929-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4e929-109">EXAMPLES</span></span>

### <span data-ttu-id="4e929-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4e929-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBGremlinGraph -ResourceGroupName {rgName} -AccountName {accountName} -DatabaseName {dbName} -Name {graphName}

Name    Id   Resource
{name}  {id} Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetPropertiesResource
```

<span data-ttu-id="4e929-111">Das Ressourcenobjekt enthält IndexingPolicy, PartitionKey, DefaultTtl, UniqueKeyPolicy, ConflictResolutionPolicy, _rid, _ts, _etag.</span><span class="sxs-lookup"><span data-stu-id="4e929-111">Resource Object contains IndexingPolicy, PartitionKey, DefaultTtl, UniqueKeyPolicy, ConflictResolutionPolicy, _rid, _ts, _etag.</span></span>

## <span data-ttu-id="4e929-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4e929-112">PARAMETERS</span></span>

### <span data-ttu-id="4e929-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="4e929-113">-AccountName</span></span>
<span data-ttu-id="4e929-114">Der Name des Dbdatenbankkontos von Db.</span><span class="sxs-lookup"><span data-stu-id="4e929-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="4e929-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="4e929-115">-DatabaseName</span></span>
<span data-ttu-id="4e929-116">Datenbankname.</span><span class="sxs-lookup"><span data-stu-id="4e929-116">Database name.</span></span>

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

### <span data-ttu-id="4e929-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e929-117">-DefaultProfile</span></span>
<span data-ttu-id="4e929-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4e929-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4e929-119">-Name</span><span class="sxs-lookup"><span data-stu-id="4e929-119">-Name</span></span>
<span data-ttu-id="4e929-120">Gremlin Graph Name.</span><span class="sxs-lookup"><span data-stu-id="4e929-120">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="4e929-121">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="4e929-121">-ParentObject</span></span>
<span data-ttu-id="4e929-122">Das Objekt "Gremlin-Datenbank".</span><span class="sxs-lookup"><span data-stu-id="4e929-122">Gremlin Database object.</span></span>

```yaml
Type: PSGremlinDatabaseGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4e929-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e929-123">-ResourceGroupName</span></span>
<span data-ttu-id="4e929-124">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="4e929-124">Name of resource group.</span></span>

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

### <span data-ttu-id="4e929-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e929-125">CommonParameters</span></span>
<span data-ttu-id="4e929-126">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e929-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e929-127">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4e929-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e929-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4e929-128">INPUTS</span></span>

### <span data-ttu-id="4e929-129">Microsoft.Azure.Commands.ExesDB.Models.PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="4e929-129">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="4e929-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4e929-130">OUTPUTS</span></span>

### <span data-ttu-id="4e929-131">Microsoft.Azure.Commands.ExesDB.Models.PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="4e929-131">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

### <span data-ttu-id="4e929-132">Microsoft.Azure.Commands.DiesDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="4e929-132">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="4e929-133">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="4e929-133">NOTES</span></span>

## <span data-ttu-id="4e929-134">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="4e929-134">RELATED LINKS</span></span>
