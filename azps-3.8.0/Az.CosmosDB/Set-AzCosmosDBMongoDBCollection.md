---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/set-azcosmosdbmongodbcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBMongoDBCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBMongoDBCollection.md
ms.openlocfilehash: 33aa465024591436d80b34b765c90badfb0f1662
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94004643"
---
# <span data-ttu-id="696bc-101">Set-AzCosmosDBMongoDBCollection</span><span class="sxs-lookup"><span data-stu-id="696bc-101">Set-AzCosmosDBMongoDBCollection</span></span>

## <span data-ttu-id="696bc-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="696bc-102">SYNOPSIS</span></span>
<span data-ttu-id="696bc-103">Legt die CosmosDB-MongoDB-Sammlung fest.</span><span class="sxs-lookup"><span data-stu-id="696bc-103">Sets the CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="696bc-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="696bc-104">SYNTAX</span></span>

### <span data-ttu-id="696bc-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="696bc-105">ByNameParameterSet (Default)</span></span>
```
Set-AzCosmosDBMongoDBCollection -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-Throughput <Int32>] [-Shard <String>] [-Index <PSMongoIndex[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="696bc-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="696bc-106">ByParentObjectParameterSet</span></span>
```
Set-AzCosmosDBMongoDBCollection -Name <String> [-Throughput <Int32>] [-Shard <String>]
 [-Index <PSMongoIndex[]>] -InputObject <PSMongoDBDatabaseGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="696bc-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="696bc-107">DESCRIPTION</span></span>
<span data-ttu-id="696bc-108">Das Cmdlet " **Set-AzCosmosDBMongoDBCollection** " legt die CosmosDB MongoDB-Sammlung fest.</span><span class="sxs-lookup"><span data-stu-id="696bc-108">The **Set-AzCosmosDBMongoDBCollection** cmdlet sets the CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="696bc-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="696bc-109">EXAMPLES</span></span>

### <span data-ttu-id="696bc-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="696bc-110">Example 1</span></span>
```powershell
PS C:\> Set-AzCosmosDBMongoDBCollection -ResourceGroupName {rgName} -AccountName {accountName}  -Database {dbName} -Name {collectionName} 

Name    Id   Resource
{name}  {id} Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetPropertiesResource
```

<span data-ttu-id="696bc-111">Das Ressourcenobjekt enthält MongoIndexes, _rid, _ts _etag Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="696bc-111">Resource Object contains MongoIndexes, _rid, _ts, _etag properties.</span></span>

## <span data-ttu-id="696bc-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="696bc-112">PARAMETERS</span></span>

### <span data-ttu-id="696bc-113">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="696bc-113">-AccountName</span></span>
<span data-ttu-id="696bc-114">Name des Cosmos DB-Daten Bankkontos.</span><span class="sxs-lookup"><span data-stu-id="696bc-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="696bc-115">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="696bc-115">-Confirm</span></span>
<span data-ttu-id="696bc-116">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="696bc-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="696bc-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="696bc-117">-DatabaseName</span></span>
<span data-ttu-id="696bc-118">Datenbankname</span><span class="sxs-lookup"><span data-stu-id="696bc-118">Database name.</span></span>

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

### <span data-ttu-id="696bc-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="696bc-119">-DefaultProfile</span></span>
<span data-ttu-id="696bc-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="696bc-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="696bc-121">-Index</span><span class="sxs-lookup"><span data-stu-id="696bc-121">-Index</span></span>
<span data-ttu-id="696bc-122">Array von PSMongoIndex-Objekten.</span><span class="sxs-lookup"><span data-stu-id="696bc-122">Array of PSMongoIndex objects.</span></span>

```yaml
Type: PSMongoIndex[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="696bc-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="696bc-123">-InputObject</span></span>
<span data-ttu-id="696bc-124">Mongo-Datenbankobjekt</span><span class="sxs-lookup"><span data-stu-id="696bc-124">Mongo Database object.</span></span>

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

### <span data-ttu-id="696bc-125">-Name</span><span class="sxs-lookup"><span data-stu-id="696bc-125">-Name</span></span>
<span data-ttu-id="696bc-126">Name der Sammlung.</span><span class="sxs-lookup"><span data-stu-id="696bc-126">Collection name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="696bc-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="696bc-127">-ResourceGroupName</span></span>
<span data-ttu-id="696bc-128">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="696bc-128">Name of resource group.</span></span>

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

### <span data-ttu-id="696bc-129">-Shard</span><span class="sxs-lookup"><span data-stu-id="696bc-129">-Shard</span></span>
<span data-ttu-id="696bc-130">Sharding-Schlüsselpfad.</span><span class="sxs-lookup"><span data-stu-id="696bc-130">Sharding key path.</span></span>

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

### <span data-ttu-id="696bc-131">-Durchsatz</span><span class="sxs-lookup"><span data-stu-id="696bc-131">-Throughput</span></span>
<span data-ttu-id="696bc-132">Der Durchsatz des SQL-Containers (ru/s).</span><span class="sxs-lookup"><span data-stu-id="696bc-132">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="696bc-133">Der Standardwert ist 400.</span><span class="sxs-lookup"><span data-stu-id="696bc-133">Default value is 400.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="696bc-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="696bc-134">-WhatIf</span></span>
<span data-ttu-id="696bc-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="696bc-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="696bc-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="696bc-136">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="696bc-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="696bc-137">CommonParameters</span></span>
<span data-ttu-id="696bc-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="696bc-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="696bc-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="696bc-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="696bc-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="696bc-140">INPUTS</span></span>

### <span data-ttu-id="696bc-141">Microsoft. Azure. Commands. CosmosDB. Models. PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="696bc-141">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

## <span data-ttu-id="696bc-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="696bc-142">OUTPUTS</span></span>

### <span data-ttu-id="696bc-143">Microsoft. Azure. Commands. CosmosDB. Models. PSMongoDBCollectionGetResults</span><span class="sxs-lookup"><span data-stu-id="696bc-143">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

## <span data-ttu-id="696bc-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="696bc-144">NOTES</span></span>

## <span data-ttu-id="696bc-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="696bc-145">RELATED LINKS</span></span>
