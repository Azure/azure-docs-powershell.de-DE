---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbmongodbcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBCollection.md
ms.openlocfilehash: 623ed0391ba36722cce26a42f1dd3d820cbd49f8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94004326"
---
# <span data-ttu-id="e8698-101">Get-AzCosmosDBMongoDBCollection</span><span class="sxs-lookup"><span data-stu-id="e8698-101">Get-AzCosmosDBMongoDBCollection</span></span>

## <span data-ttu-id="e8698-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e8698-102">SYNOPSIS</span></span>
<span data-ttu-id="e8698-103">Ruft die CosmosDB MongoDB-Sammlung ab.</span><span class="sxs-lookup"><span data-stu-id="e8698-103">Gets the CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="e8698-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e8698-104">SYNTAX</span></span>

### <span data-ttu-id="e8698-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="e8698-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBMongoDBCollection -ResourceGroupName <String> [-Name <String>] [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] -AccountName <String> -DatabaseName <String> [<CommonParameters>]
```

### <span data-ttu-id="e8698-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e8698-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBMongoDBCollection [-Name <String>] -InputObject <PSMongoDBDatabaseGetResults> [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e8698-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e8698-107">DESCRIPTION</span></span>
<span data-ttu-id="e8698-108">Das Cmdlet " **Get-AzCosmosDBMongoDBCollection** " Ruft die CosmosDB MongoDB-Sammlung ab.</span><span class="sxs-lookup"><span data-stu-id="e8698-108">The **Get-AzCosmosDBMongoDBCollection** cmdlet gets the CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="e8698-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e8698-109">EXAMPLES</span></span>

### <span data-ttu-id="e8698-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e8698-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBMongoDBCollection -ResourceGroupName {rgName} -AccountName {accountName}  -Database {dbName} -Name {collectionName} 

Name    Id   Resource
{name}  {id} Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetPropertiesResource
```

<span data-ttu-id="e8698-111">Das Ressourcenobjekt enthält MongoIndexes, _rid, _ts _etag Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="e8698-111">Resource Object contains MongoIndexes, _rid, _ts, _etag properties.</span></span>

## <span data-ttu-id="e8698-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="e8698-112">PARAMETERS</span></span>

### <span data-ttu-id="e8698-113">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="e8698-113">-AccountName</span></span>
<span data-ttu-id="e8698-114">Name des Cosmos DB-Daten Bankkontos.</span><span class="sxs-lookup"><span data-stu-id="e8698-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="e8698-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e8698-115">-DatabaseName</span></span>
<span data-ttu-id="e8698-116">Datenbankname</span><span class="sxs-lookup"><span data-stu-id="e8698-116">Database name.</span></span>

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

### <span data-ttu-id="e8698-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8698-117">-DefaultProfile</span></span>
<span data-ttu-id="e8698-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e8698-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e8698-119">-Detailliert</span><span class="sxs-lookup"><span data-stu-id="e8698-119">-Detailed</span></span>
<span data-ttu-id="e8698-120">Wenn Sie dann bereitgestellt werden, gibt das Cmdlet die Auflistung mit dem entsprechenden Durchsatz zurück.</span><span class="sxs-lookup"><span data-stu-id="e8698-120">If provided then, the cmdlet returns the collection with the corresponding throughput value.</span></span>

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

### <span data-ttu-id="e8698-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="e8698-121">-InputObject</span></span>
<span data-ttu-id="e8698-122">Mongo-Datenbankobjekt</span><span class="sxs-lookup"><span data-stu-id="e8698-122">Mongo Database object.</span></span>

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

### <span data-ttu-id="e8698-123">-Name</span><span class="sxs-lookup"><span data-stu-id="e8698-123">-Name</span></span>
<span data-ttu-id="e8698-124">Name der Sammlung.</span><span class="sxs-lookup"><span data-stu-id="e8698-124">Collection name.</span></span>

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

### <span data-ttu-id="e8698-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8698-125">-ResourceGroupName</span></span>
<span data-ttu-id="e8698-126">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="e8698-126">Name of resource group.</span></span>

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

### <span data-ttu-id="e8698-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8698-127">CommonParameters</span></span>
<span data-ttu-id="e8698-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8698-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8698-129">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e8698-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8698-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e8698-130">INPUTS</span></span>

### <span data-ttu-id="e8698-131">Microsoft. Azure. Commands. CosmosDB. Models. PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="e8698-131">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

## <span data-ttu-id="e8698-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e8698-132">OUTPUTS</span></span>

### <span data-ttu-id="e8698-133">Microsoft. Azure. Commands. CosmosDB. Models. PSMongoDBCollectionGetResults</span><span class="sxs-lookup"><span data-stu-id="e8698-133">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

### <span data-ttu-id="e8698-134">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="e8698-134">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="e8698-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="e8698-135">NOTES</span></span>

## <span data-ttu-id="e8698-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e8698-136">RELATED LINKS</span></span>
