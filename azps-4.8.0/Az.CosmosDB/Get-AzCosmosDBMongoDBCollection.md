---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbmongodbcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBCollection.md
ms.openlocfilehash: 1919b3075b24e96edce93c8d3611f3864d3f9391
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94167269"
---
# <span data-ttu-id="f68c1-101">Get-AzCosmosDBMongoDBCollection</span><span class="sxs-lookup"><span data-stu-id="f68c1-101">Get-AzCosmosDBMongoDBCollection</span></span>

## <span data-ttu-id="f68c1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f68c1-102">SYNOPSIS</span></span>
<span data-ttu-id="f68c1-103">Ruft die CosmosDB MongoDB-Sammlung ab.</span><span class="sxs-lookup"><span data-stu-id="f68c1-103">Gets the CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="f68c1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f68c1-104">SYNTAX</span></span>

### <span data-ttu-id="f68c1-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="f68c1-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBMongoDBCollection -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] -AccountName <String> -DatabaseName <String> [<CommonParameters>]
```

### <span data-ttu-id="f68c1-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f68c1-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBMongoDBCollection [-Name <String>] -ParentObject <PSMongoDBDatabaseGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f68c1-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f68c1-107">DESCRIPTION</span></span>
<span data-ttu-id="f68c1-108">Das Cmdlet " **Get-AzCosmosDBMongoDBCollection** " Ruft die CosmosDB MongoDB-Sammlung ab.</span><span class="sxs-lookup"><span data-stu-id="f68c1-108">The **Get-AzCosmosDBMongoDBCollection** cmdlet gets the CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="f68c1-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f68c1-109">EXAMPLES</span></span>

### <span data-ttu-id="f68c1-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f68c1-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBMongoDBCollection -ResourceGroupName {rgName} -AccountName {accountName} -Database {dbName} -Name {collectionName} 

Name    Id   Resource
{name}  {id} Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetPropertiesResource
```

<span data-ttu-id="f68c1-111">Das Ressourcenobjekt enthält MongoIndexes, _rid, _ts _etag Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="f68c1-111">Resource Object contains MongoIndexes, _rid, _ts, _etag properties.</span></span>

### <span data-ttu-id="f68c1-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="f68c1-112">Example 2</span></span>
```powershell
PS C:\> (Get-AzCosmosDBMongoDBCollection -ResourceGroupName {rgName} -AccountName {accountName} -Database {dbName} -Name {collectionName}).Resource.ShardKey 

Key           Value
----          ----- 
<ShardKey>    <Value>
```

<span data-ttu-id="f68c1-113">In diesem Beispiel wird die ShardKey der abgerufenen Sammlung abgerufen.</span><span class="sxs-lookup"><span data-stu-id="f68c1-113">This example gets the ShardKey of the retrieved collection</span></span>

## <span data-ttu-id="f68c1-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="f68c1-114">PARAMETERS</span></span>

### <span data-ttu-id="f68c1-115">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="f68c1-115">-AccountName</span></span>
<span data-ttu-id="f68c1-116">Name des Cosmos DB-Daten Bankkontos.</span><span class="sxs-lookup"><span data-stu-id="f68c1-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="f68c1-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f68c1-117">-DatabaseName</span></span>
<span data-ttu-id="f68c1-118">Datenbankname</span><span class="sxs-lookup"><span data-stu-id="f68c1-118">Database name.</span></span>

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

### <span data-ttu-id="f68c1-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f68c1-119">-DefaultProfile</span></span>
<span data-ttu-id="f68c1-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f68c1-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f68c1-121">-Name</span><span class="sxs-lookup"><span data-stu-id="f68c1-121">-Name</span></span>
<span data-ttu-id="f68c1-122">Name der Sammlung.</span><span class="sxs-lookup"><span data-stu-id="f68c1-122">Collection name.</span></span>

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

### <span data-ttu-id="f68c1-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="f68c1-123">-ParentObject</span></span>
<span data-ttu-id="f68c1-124">Mongo-Datenbankobjekt</span><span class="sxs-lookup"><span data-stu-id="f68c1-124">Mongo Database object.</span></span>

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

### <span data-ttu-id="f68c1-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f68c1-125">-ResourceGroupName</span></span>
<span data-ttu-id="f68c1-126">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="f68c1-126">Name of resource group.</span></span>

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

### <span data-ttu-id="f68c1-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f68c1-127">CommonParameters</span></span>
<span data-ttu-id="f68c1-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f68c1-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f68c1-129">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f68c1-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f68c1-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f68c1-130">INPUTS</span></span>

### <span data-ttu-id="f68c1-131">Microsoft. Azure. Commands. CosmosDB. Models. PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="f68c1-131">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

## <span data-ttu-id="f68c1-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f68c1-132">OUTPUTS</span></span>

### <span data-ttu-id="f68c1-133">Microsoft. Azure. Commands. CosmosDB. Models. PSMongoDBCollectionGetResults</span><span class="sxs-lookup"><span data-stu-id="f68c1-133">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

### <span data-ttu-id="f68c1-134">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="f68c1-134">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="f68c1-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="f68c1-135">NOTES</span></span>

## <span data-ttu-id="f68c1-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f68c1-136">RELATED LINKS</span></span>
