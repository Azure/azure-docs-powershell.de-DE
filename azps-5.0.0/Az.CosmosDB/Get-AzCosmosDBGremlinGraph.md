---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbgremlingraph
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinGraph.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinGraph.md
ms.openlocfilehash: 1b8bcbdeb797aea0faa5e9b3a0b5cb1e36b0f1b9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94299548"
---
# <span data-ttu-id="07460-101">Get-AzCosmosDBGremlinGraph</span><span class="sxs-lookup"><span data-stu-id="07460-101">Get-AzCosmosDBGremlinGraph</span></span>

## <span data-ttu-id="07460-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="07460-102">SYNOPSIS</span></span>
<span data-ttu-id="07460-103">Ruft das CosmosDB-Gremlin-Diagramm ab.</span><span class="sxs-lookup"><span data-stu-id="07460-103">Gets the CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="07460-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="07460-104">SYNTAX</span></span>

### <span data-ttu-id="07460-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="07460-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBGremlinGraph -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] -AccountName <String> -DatabaseName <String> [<CommonParameters>]
```

### <span data-ttu-id="07460-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="07460-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBGremlinGraph [-Name <String>] -ParentObject <PSGremlinDatabaseGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="07460-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="07460-107">DESCRIPTION</span></span>
<span data-ttu-id="07460-108">Das Cmdlet " **Get-AzCosmosDBGremlinGraph** " Ruft die CosmosDB Gremlin-Diagrammeigenschaften ab.</span><span class="sxs-lookup"><span data-stu-id="07460-108">The **Get-AzCosmosDBGremlinGraph** cmdlet gets the CosmosDB Gremlin Graph properties.</span></span>

## <span data-ttu-id="07460-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="07460-109">EXAMPLES</span></span>

### <span data-ttu-id="07460-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="07460-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBGremlinGraph -ResourceGroupName {rgName} -AccountName {accountName} -DatabaseName {dbName} -Name {graphName}

Name    Id   Resource
{name}  {id} Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetPropertiesResource
```

<span data-ttu-id="07460-111">Das Ressourcenobjekt enthält IndexingPolicy, PartitionKey, DefaultTtl, UniqueKeyPolicy, ConflictResolutionPolicy, _rid, _ts, _etag.</span><span class="sxs-lookup"><span data-stu-id="07460-111">Resource Object contains IndexingPolicy, PartitionKey, DefaultTtl, UniqueKeyPolicy, ConflictResolutionPolicy, _rid, _ts, _etag.</span></span>

## <span data-ttu-id="07460-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="07460-112">PARAMETERS</span></span>

### <span data-ttu-id="07460-113">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="07460-113">-AccountName</span></span>
<span data-ttu-id="07460-114">Name des Cosmos DB-Daten Bankkontos.</span><span class="sxs-lookup"><span data-stu-id="07460-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="07460-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="07460-115">-DatabaseName</span></span>
<span data-ttu-id="07460-116">Datenbankname</span><span class="sxs-lookup"><span data-stu-id="07460-116">Database name.</span></span>

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

### <span data-ttu-id="07460-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07460-117">-DefaultProfile</span></span>
<span data-ttu-id="07460-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="07460-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="07460-119">-Name</span><span class="sxs-lookup"><span data-stu-id="07460-119">-Name</span></span>
<span data-ttu-id="07460-120">Gremlin-Diagramm Name</span><span class="sxs-lookup"><span data-stu-id="07460-120">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="07460-121">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="07460-121">-ParentObject</span></span>
<span data-ttu-id="07460-122">Gremlin-Datenbankobjekt.</span><span class="sxs-lookup"><span data-stu-id="07460-122">Gremlin Database object.</span></span>

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

### <span data-ttu-id="07460-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07460-123">-ResourceGroupName</span></span>
<span data-ttu-id="07460-124">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="07460-124">Name of resource group.</span></span>

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

### <span data-ttu-id="07460-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07460-125">CommonParameters</span></span>
<span data-ttu-id="07460-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07460-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07460-127">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="07460-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07460-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="07460-128">INPUTS</span></span>

### <span data-ttu-id="07460-129">Microsoft. Azure. Commands. CosmosDB. Models. PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="07460-129">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="07460-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="07460-130">OUTPUTS</span></span>

### <span data-ttu-id="07460-131">Microsoft. Azure. Commands. CosmosDB. Models. PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="07460-131">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

### <span data-ttu-id="07460-132">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="07460-132">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="07460-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="07460-133">NOTES</span></span>

## <span data-ttu-id="07460-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="07460-134">RELATED LINKS</span></span>
