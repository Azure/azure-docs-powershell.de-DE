---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/get-azcosmosdbgremlingraph
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinGraph.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinGraph.md
ms.openlocfilehash: 4818f0bb179274181c998c4ad07ca013ade0a2b3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101934427"
---
# <span data-ttu-id="828f7-101">Get-AzCosmosDBGremlinGraph</span><span class="sxs-lookup"><span data-stu-id="828f7-101">Get-AzCosmosDBGremlinGraph</span></span>

## <span data-ttu-id="828f7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="828f7-102">SYNOPSIS</span></span>
<span data-ttu-id="828f7-103">Ruft die CosmosDB Gremlin Graph ab.</span><span class="sxs-lookup"><span data-stu-id="828f7-103">Gets the CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="828f7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="828f7-104">SYNTAX</span></span>

### <span data-ttu-id="828f7-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="828f7-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBGremlinGraph -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] -AccountName <String> -DatabaseName <String> [<CommonParameters>]
```

### <span data-ttu-id="828f7-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="828f7-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBGremlinGraph [-Name <String>] -ParentObject <PSGremlinDatabaseGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="828f7-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="828f7-107">DESCRIPTION</span></span>
<span data-ttu-id="828f7-108">Das **Cmdlet Get-AzCosmosDBGremlinGraph** ruft die Eigenschaften von CosmosDB Gremlin Graph ab.</span><span class="sxs-lookup"><span data-stu-id="828f7-108">The **Get-AzCosmosDBGremlinGraph** cmdlet gets the CosmosDB Gremlin Graph properties.</span></span>

## <span data-ttu-id="828f7-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="828f7-109">EXAMPLES</span></span>

### <span data-ttu-id="828f7-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="828f7-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBGremlinGraph -ResourceGroupName {rgName} -AccountName {accountName} -DatabaseName {dbName} -Name {graphName}

Name    Id   Resource
{name}  {id} Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetPropertiesResource
```

<span data-ttu-id="828f7-111">Ressourcenobjekt enthält IndexingPolicy, PartitionKey, DefaultTtl, UniqueKeyPolicy, ConflictResolutionPolicy, _rid, _ts, _etag.</span><span class="sxs-lookup"><span data-stu-id="828f7-111">Resource Object contains IndexingPolicy, PartitionKey, DefaultTtl, UniqueKeyPolicy, ConflictResolutionPolicy, _rid, _ts, _etag.</span></span>

## <span data-ttu-id="828f7-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="828f7-112">PARAMETERS</span></span>

### <span data-ttu-id="828f7-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="828f7-113">-AccountName</span></span>
<span data-ttu-id="828f7-114">Name des Datenbankkontos "Cosmos DB".</span><span class="sxs-lookup"><span data-stu-id="828f7-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="828f7-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="828f7-115">-DatabaseName</span></span>
<span data-ttu-id="828f7-116">Datenbankname.</span><span class="sxs-lookup"><span data-stu-id="828f7-116">Database name.</span></span>

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

### <span data-ttu-id="828f7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="828f7-117">-DefaultProfile</span></span>
<span data-ttu-id="828f7-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="828f7-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="828f7-119">-Name</span><span class="sxs-lookup"><span data-stu-id="828f7-119">-Name</span></span>
<span data-ttu-id="828f7-120">Gremlin Graph Name.</span><span class="sxs-lookup"><span data-stu-id="828f7-120">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="828f7-121">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="828f7-121">-ParentObject</span></span>
<span data-ttu-id="828f7-122">Gremlin-Datenbankobjekt.</span><span class="sxs-lookup"><span data-stu-id="828f7-122">Gremlin Database object.</span></span>

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

### <span data-ttu-id="828f7-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="828f7-123">-ResourceGroupName</span></span>
<span data-ttu-id="828f7-124">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="828f7-124">Name of resource group.</span></span>

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

### <span data-ttu-id="828f7-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="828f7-125">CommonParameters</span></span>
<span data-ttu-id="828f7-126">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="828f7-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="828f7-127">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="828f7-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="828f7-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="828f7-128">INPUTS</span></span>

### <span data-ttu-id="828f7-129">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="828f7-129">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="828f7-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="828f7-130">OUTPUTS</span></span>

### <span data-ttu-id="828f7-131">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="828f7-131">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

### <span data-ttu-id="828f7-132">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="828f7-132">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="828f7-133">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="828f7-133">NOTES</span></span>

## <span data-ttu-id="828f7-134">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="828f7-134">RELATED LINKS</span></span>
