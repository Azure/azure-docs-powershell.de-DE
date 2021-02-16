---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbmongodbcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBCollection.md
ms.openlocfilehash: 1919b3075b24e96edce93c8d3611f3864d3f9391
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100171054"
---
# <span data-ttu-id="d1ab5-101">Get-AzCosmosDBMongoDBCollection</span><span class="sxs-lookup"><span data-stu-id="d1ab5-101">Get-AzCosmosDBMongoDBCollection</span></span>

## <span data-ttu-id="d1ab5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d1ab5-102">SYNOPSIS</span></span>
<span data-ttu-id="d1ab5-103">Ruft die AbosDB MongoDB Collection ab.</span><span class="sxs-lookup"><span data-stu-id="d1ab5-103">Gets the CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="d1ab5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d1ab5-104">SYNTAX</span></span>

### <span data-ttu-id="d1ab5-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="d1ab5-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBMongoDBCollection -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] -AccountName <String> -DatabaseName <String> [<CommonParameters>]
```

### <span data-ttu-id="d1ab5-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d1ab5-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBMongoDBCollection [-Name <String>] -ParentObject <PSMongoDBDatabaseGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d1ab5-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d1ab5-107">DESCRIPTION</span></span>
<span data-ttu-id="d1ab5-108">Das **Cmdlet "Get-AzCosmosDBMongoDBCollection"** ruft die "DessDB MongoDB Collection" ab.</span><span class="sxs-lookup"><span data-stu-id="d1ab5-108">The **Get-AzCosmosDBMongoDBCollection** cmdlet gets the CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="d1ab5-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d1ab5-109">EXAMPLES</span></span>

### <span data-ttu-id="d1ab5-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d1ab5-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBMongoDBCollection -ResourceGroupName {rgName} -AccountName {accountName} -Database {dbName} -Name {collectionName} 

Name    Id   Resource
{name}  {id} Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetPropertiesResource
```

<span data-ttu-id="d1ab5-111">Das Ressourcenobjekt enthält "MongoIndexes", "_rid", "_ts" _etag "_etag".</span><span class="sxs-lookup"><span data-stu-id="d1ab5-111">Resource Object contains MongoIndexes, _rid, _ts, _etag properties.</span></span>

### <span data-ttu-id="d1ab5-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="d1ab5-112">Example 2</span></span>
```powershell
PS C:\> (Get-AzCosmosDBMongoDBCollection -ResourceGroupName {rgName} -AccountName {accountName} -Database {dbName} -Name {collectionName}).Resource.ShardKey 

Key           Value
----          ----- 
<ShardKey>    <Value>
```

<span data-ttu-id="d1ab5-113">In diesem Beispiel wird der ShardKey der abgerufenen Auflistung abgerufen.</span><span class="sxs-lookup"><span data-stu-id="d1ab5-113">This example gets the ShardKey of the retrieved collection</span></span>

## <span data-ttu-id="d1ab5-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d1ab5-114">PARAMETERS</span></span>

### <span data-ttu-id="d1ab5-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="d1ab5-115">-AccountName</span></span>
<span data-ttu-id="d1ab5-116">Der Name des Dbdatenbankkontos von Db.</span><span class="sxs-lookup"><span data-stu-id="d1ab5-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="d1ab5-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d1ab5-117">-DatabaseName</span></span>
<span data-ttu-id="d1ab5-118">Datenbankname.</span><span class="sxs-lookup"><span data-stu-id="d1ab5-118">Database name.</span></span>

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

### <span data-ttu-id="d1ab5-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1ab5-119">-DefaultProfile</span></span>
<span data-ttu-id="d1ab5-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d1ab5-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d1ab5-121">-Name</span><span class="sxs-lookup"><span data-stu-id="d1ab5-121">-Name</span></span>
<span data-ttu-id="d1ab5-122">Sammlungsname.</span><span class="sxs-lookup"><span data-stu-id="d1ab5-122">Collection name.</span></span>

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

### <span data-ttu-id="d1ab5-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="d1ab5-123">-ParentObject</span></span>
<span data-ttu-id="d1ab5-124">Mongo-Datenbankobjekt.</span><span class="sxs-lookup"><span data-stu-id="d1ab5-124">Mongo Database object.</span></span>

```yaml
Type: PSMongoDBDatabaseGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d1ab5-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1ab5-125">-ResourceGroupName</span></span>
<span data-ttu-id="d1ab5-126">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="d1ab5-126">Name of resource group.</span></span>

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

### <span data-ttu-id="d1ab5-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1ab5-127">CommonParameters</span></span>
<span data-ttu-id="d1ab5-128">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1ab5-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1ab5-129">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d1ab5-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1ab5-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d1ab5-130">INPUTS</span></span>

### <span data-ttu-id="d1ab5-131">Microsoft.Azure.Commands.ExesDB.Models.PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="d1ab5-131">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

## <span data-ttu-id="d1ab5-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d1ab5-132">OUTPUTS</span></span>

### <span data-ttu-id="d1ab5-133">Microsoft.Azure.Commands.ExesDB.Models.PSMongoDBCollectionGetResults</span><span class="sxs-lookup"><span data-stu-id="d1ab5-133">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

### <span data-ttu-id="d1ab5-134">Microsoft.Azure.Commands.ExesDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="d1ab5-134">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="d1ab5-135">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="d1ab5-135">NOTES</span></span>

## <span data-ttu-id="d1ab5-136">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="d1ab5-136">RELATED LINKS</span></span>
