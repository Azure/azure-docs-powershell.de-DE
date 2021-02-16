---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbmongodbcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBMongoDBCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBMongoDBCollection.md
ms.openlocfilehash: 741d63bfe54c03eb101d74519251b67c5e1664b1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100148545"
---
# <span data-ttu-id="53694-101">New-AzCosmosDBMongoDBCollection</span><span class="sxs-lookup"><span data-stu-id="53694-101">New-AzCosmosDBMongoDBCollection</span></span>

## <span data-ttu-id="53694-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="53694-102">SYNOPSIS</span></span>
<span data-ttu-id="53694-103">Erstellt eine neue AbosDB MongoDB-Sammlung.</span><span class="sxs-lookup"><span data-stu-id="53694-103">Creates a new CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="53694-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="53694-104">SYNTAX</span></span>

### <span data-ttu-id="53694-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="53694-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBMongoDBCollection -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-Shard <String>]
 [-AnalyticalStorageTtl <Int32>] [-Index <PSMongoIndex[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="53694-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="53694-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBMongoDBCollection -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-Shard <String>] [-AnalyticalStorageTtl <Int32>] [-Index <PSMongoIndex[]>]
 -ParentObject <PSMongoDBDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="53694-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="53694-107">DESCRIPTION</span></span>
<span data-ttu-id="53694-108">Erstellt eine neue AbosDB MongoDB-Sammlung.</span><span class="sxs-lookup"><span data-stu-id="53694-108">Creates a new CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="53694-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="53694-109">EXAMPLES</span></span>

### <span data-ttu-id="53694-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="53694-110">Example 1</span></span>
```powershell
PS C:\> 
        $ttlInSeconds = 604800
        $index1 = New-AzCosmosDBMongoDBIndex -Key @("partitionkey1", "partitionkey2") -Unique 1
>>      $index2 = New-AzCosmosDBMongoDBIndex -Key @("_ts") -TtlInSeconds $ttlInSeconds

New-AzCosmosDBMongoDBCollection -AccountName myAccountName -ResourceGroupName myRgName -DatabaseName myDatabaseName -Name myCollectionName -Index $index1,$index2 -Shard myShardKey

Name     : collection1
Id       : /subscriptions/mySubId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/mongodbDatabases/myDatabaseName/collect
           ions/myCollectionName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetPropertiesResource
```

## <span data-ttu-id="53694-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="53694-111">PARAMETERS</span></span>

### <span data-ttu-id="53694-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="53694-112">-AccountName</span></span>
<span data-ttu-id="53694-113">Der Name des Dbdatenbankkontos von Db.</span><span class="sxs-lookup"><span data-stu-id="53694-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="53694-114">-AnalyticalStorageTtl</span><span class="sxs-lookup"><span data-stu-id="53694-114">-AnalyticalStorageTtl</span></span>
<span data-ttu-id="53694-115">TTL für Analysespeicher.</span><span class="sxs-lookup"><span data-stu-id="53694-115">TTL for Analytical Storage.</span></span>

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

### <span data-ttu-id="53694-116">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="53694-116">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="53694-117">Der maximale Durchsatzwert, wenn die Automatische Skalierung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="53694-117">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="53694-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="53694-118">-Confirm</span></span>
<span data-ttu-id="53694-119">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="53694-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="53694-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="53694-120">-DatabaseName</span></span>
<span data-ttu-id="53694-121">Datenbankname.</span><span class="sxs-lookup"><span data-stu-id="53694-121">Database name.</span></span>

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

### <span data-ttu-id="53694-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53694-122">-DefaultProfile</span></span>
<span data-ttu-id="53694-123">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="53694-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="53694-124">-Index</span><span class="sxs-lookup"><span data-stu-id="53694-124">-Index</span></span>
<span data-ttu-id="53694-125">Array von PSMongoIndex-Objekten.</span><span class="sxs-lookup"><span data-stu-id="53694-125">Array of PSMongoIndex objects.</span></span>

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

### <span data-ttu-id="53694-126">-Name</span><span class="sxs-lookup"><span data-stu-id="53694-126">-Name</span></span>
<span data-ttu-id="53694-127">Sammlungsname.</span><span class="sxs-lookup"><span data-stu-id="53694-127">Collection name.</span></span>

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

### <span data-ttu-id="53694-128">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="53694-128">-ParentObject</span></span>
<span data-ttu-id="53694-129">Mongo-Datenbankobjekt.</span><span class="sxs-lookup"><span data-stu-id="53694-129">Mongo Database object.</span></span>

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

### <span data-ttu-id="53694-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53694-130">-ResourceGroupName</span></span>
<span data-ttu-id="53694-131">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="53694-131">Name of resource group.</span></span>

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

### <span data-ttu-id="53694-132">-Shard</span><span class="sxs-lookup"><span data-stu-id="53694-132">-Shard</span></span>
<span data-ttu-id="53694-133">Shardingschlüsselpfad</span><span class="sxs-lookup"><span data-stu-id="53694-133">Sharding key path.</span></span>

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

### <span data-ttu-id="53694-134">-Throughput</span><span class="sxs-lookup"><span data-stu-id="53694-134">-Throughput</span></span>
<span data-ttu-id="53694-135">Der Durchsatz SQL Container (RU/s).</span><span class="sxs-lookup"><span data-stu-id="53694-135">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="53694-136">Der Standardwert ist 400.</span><span class="sxs-lookup"><span data-stu-id="53694-136">Default value is 400.</span></span>

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

### <span data-ttu-id="53694-137">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="53694-137">-WhatIf</span></span>
<span data-ttu-id="53694-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="53694-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="53694-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="53694-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="53694-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53694-140">CommonParameters</span></span>
<span data-ttu-id="53694-141">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53694-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53694-142">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="53694-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53694-143">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="53694-143">INPUTS</span></span>

### <span data-ttu-id="53694-144">Microsoft.Azure.Commands.ExesDB.Models.PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="53694-144">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

## <span data-ttu-id="53694-145">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="53694-145">OUTPUTS</span></span>

### <span data-ttu-id="53694-146">Microsoft.Azure.Commands.ExesDB.Models.PSMongoDBCollectionGetResults</span><span class="sxs-lookup"><span data-stu-id="53694-146">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

### <span data-ttu-id="53694-147">Microsoft.Azure.Commands.DiesDB.Exceptions.ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="53694-147">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="53694-148">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="53694-148">NOTES</span></span>

## <span data-ttu-id="53694-149">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="53694-149">RELATED LINKS</span></span>
