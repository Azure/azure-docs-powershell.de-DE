---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbgremlingraph
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinGraph.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinGraph.md
ms.openlocfilehash: 2da3a5729673abde6ad54ea66f1b5fbd9f089db9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94004328"
---
# <span data-ttu-id="b1891-101">Get-AzCosmosDBGremlinGraph</span><span class="sxs-lookup"><span data-stu-id="b1891-101">Get-AzCosmosDBGremlinGraph</span></span>

## <span data-ttu-id="b1891-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b1891-102">SYNOPSIS</span></span>
<span data-ttu-id="b1891-103">Ruft das CosmosDB-Gremlin-Diagramm ab.</span><span class="sxs-lookup"><span data-stu-id="b1891-103">Gets the CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="b1891-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b1891-104">SYNTAX</span></span>

### <span data-ttu-id="b1891-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="b1891-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBGremlinGraph -ResourceGroupName <String> [-Name <String>] [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] -AccountName <String> -DatabaseName <String> [<CommonParameters>]
```

### <span data-ttu-id="b1891-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b1891-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBGremlinGraph [-Name <String>] -InputObject <PSGremlinDatabaseGetResults> [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b1891-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b1891-107">DESCRIPTION</span></span>
<span data-ttu-id="b1891-108">Das Cmdlet " **Get-AzCosmosDBGremlinGraph** " Ruft die CosmosDB Gremlin-Diagrammeigenschaften ab.</span><span class="sxs-lookup"><span data-stu-id="b1891-108">The **Get-AzCosmosDBGremlinGraph** cmdlet gets the CosmosDB Gremlin Graph properties.</span></span>

## <span data-ttu-id="b1891-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b1891-109">EXAMPLES</span></span>

### <span data-ttu-id="b1891-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b1891-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBGremlinGraph -ResourceGroupName {rgName} -AccountName {accountName} -DatabaseName {dbName} -Name {graphName}

Name    Id   Resource
{name}  {id} Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetPropertiesResource
```

<span data-ttu-id="b1891-111">Das Ressourcenobjekt enthält IndexingPolicy, PartitionKey, DefaultTtl, UniqueKeyPolicy, ConflictResolutionPolicy, _rid, _ts, _etag.</span><span class="sxs-lookup"><span data-stu-id="b1891-111">Resource Object contains IndexingPolicy, PartitionKey, DefaultTtl, UniqueKeyPolicy, ConflictResolutionPolicy, _rid, _ts, _etag.</span></span>

## <span data-ttu-id="b1891-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="b1891-112">PARAMETERS</span></span>

### <span data-ttu-id="b1891-113">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="b1891-113">-AccountName</span></span>
<span data-ttu-id="b1891-114">Name des Cosmos DB-Daten Bankkontos.</span><span class="sxs-lookup"><span data-stu-id="b1891-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="b1891-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b1891-115">-DatabaseName</span></span>
<span data-ttu-id="b1891-116">Datenbankname</span><span class="sxs-lookup"><span data-stu-id="b1891-116">Database name.</span></span>

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

### <span data-ttu-id="b1891-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1891-117">-DefaultProfile</span></span>
<span data-ttu-id="b1891-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b1891-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b1891-119">-Detailliert</span><span class="sxs-lookup"><span data-stu-id="b1891-119">-Detailed</span></span>
<span data-ttu-id="b1891-120">Wenn Sie dann bereitgestellt werden, gibt das Cmdlet das Gremlin-Diagramm mit dem entsprechenden Durchsatz zurück.</span><span class="sxs-lookup"><span data-stu-id="b1891-120">If provided then, the cmdlet returns the Gremlin Graph with the corresponding throughput value.</span></span>

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

### <span data-ttu-id="b1891-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="b1891-121">-InputObject</span></span>
<span data-ttu-id="b1891-122">Gremlin-Datenbankobjekt.</span><span class="sxs-lookup"><span data-stu-id="b1891-122">Gremlin Database object.</span></span>

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

### <span data-ttu-id="b1891-123">-Name</span><span class="sxs-lookup"><span data-stu-id="b1891-123">-Name</span></span>
<span data-ttu-id="b1891-124">Gremlin-Diagramm Name</span><span class="sxs-lookup"><span data-stu-id="b1891-124">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="b1891-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1891-125">-ResourceGroupName</span></span>
<span data-ttu-id="b1891-126">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="b1891-126">Name of resource group.</span></span>

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

### <span data-ttu-id="b1891-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1891-127">CommonParameters</span></span>
<span data-ttu-id="b1891-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1891-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1891-129">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b1891-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1891-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b1891-130">INPUTS</span></span>

### <span data-ttu-id="b1891-131">Microsoft. Azure. Commands. CosmosDB. Models. PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="b1891-131">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="b1891-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b1891-132">OUTPUTS</span></span>

### <span data-ttu-id="b1891-133">Microsoft. Azure. Commands. CosmosDB. Models. PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="b1891-133">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

### <span data-ttu-id="b1891-134">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="b1891-134">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="b1891-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="b1891-135">NOTES</span></span>

## <span data-ttu-id="b1891-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b1891-136">RELATED LINKS</span></span>
