---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbmongodbcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBMongoDBCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBMongoDBCollection.md
ms.openlocfilehash: 741d63bfe54c03eb101d74519251b67c5e1664b1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94299290"
---
# <span data-ttu-id="5623c-101">New-AzCosmosDBMongoDBCollection</span><span class="sxs-lookup"><span data-stu-id="5623c-101">New-AzCosmosDBMongoDBCollection</span></span>

## <span data-ttu-id="5623c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5623c-102">SYNOPSIS</span></span>
<span data-ttu-id="5623c-103">Erstellt eine neue CosmosDB-MongoDB-Sammlung.</span><span class="sxs-lookup"><span data-stu-id="5623c-103">Creates a new CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="5623c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5623c-104">SYNTAX</span></span>

### <span data-ttu-id="5623c-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="5623c-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBMongoDBCollection -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-Shard <String>]
 [-AnalyticalStorageTtl <Int32>] [-Index <PSMongoIndex[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5623c-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5623c-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBMongoDBCollection -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-Shard <String>] [-AnalyticalStorageTtl <Int32>] [-Index <PSMongoIndex[]>]
 -ParentObject <PSMongoDBDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5623c-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5623c-107">DESCRIPTION</span></span>
<span data-ttu-id="5623c-108">Erstellt eine neue CosmosDB-MongoDB-Sammlung.</span><span class="sxs-lookup"><span data-stu-id="5623c-108">Creates a new CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="5623c-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5623c-109">EXAMPLES</span></span>

### <span data-ttu-id="5623c-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5623c-110">Example 1</span></span>
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

## <span data-ttu-id="5623c-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="5623c-111">PARAMETERS</span></span>

### <span data-ttu-id="5623c-112">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="5623c-112">-AccountName</span></span>
<span data-ttu-id="5623c-113">Name des Cosmos DB-Daten Bankkontos.</span><span class="sxs-lookup"><span data-stu-id="5623c-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="5623c-114">-AnalyticalStorageTtl</span><span class="sxs-lookup"><span data-stu-id="5623c-114">-AnalyticalStorageTtl</span></span>
<span data-ttu-id="5623c-115">TTL für Analyse Speicher.</span><span class="sxs-lookup"><span data-stu-id="5623c-115">TTL for Analytical Storage.</span></span>

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

### <span data-ttu-id="5623c-116">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="5623c-116">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="5623c-117">Maximaler Durchsatz, wenn "AutoScale" aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="5623c-117">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="5623c-118">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5623c-118">-Confirm</span></span>
<span data-ttu-id="5623c-119">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5623c-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5623c-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="5623c-120">-DatabaseName</span></span>
<span data-ttu-id="5623c-121">Datenbankname</span><span class="sxs-lookup"><span data-stu-id="5623c-121">Database name.</span></span>

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

### <span data-ttu-id="5623c-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5623c-122">-DefaultProfile</span></span>
<span data-ttu-id="5623c-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5623c-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5623c-124">-Index</span><span class="sxs-lookup"><span data-stu-id="5623c-124">-Index</span></span>
<span data-ttu-id="5623c-125">Array von PSMongoIndex-Objekten.</span><span class="sxs-lookup"><span data-stu-id="5623c-125">Array of PSMongoIndex objects.</span></span>

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

### <span data-ttu-id="5623c-126">-Name</span><span class="sxs-lookup"><span data-stu-id="5623c-126">-Name</span></span>
<span data-ttu-id="5623c-127">Name der Sammlung.</span><span class="sxs-lookup"><span data-stu-id="5623c-127">Collection name.</span></span>

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

### <span data-ttu-id="5623c-128">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="5623c-128">-ParentObject</span></span>
<span data-ttu-id="5623c-129">Mongo-Datenbankobjekt</span><span class="sxs-lookup"><span data-stu-id="5623c-129">Mongo Database object.</span></span>

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

### <span data-ttu-id="5623c-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5623c-130">-ResourceGroupName</span></span>
<span data-ttu-id="5623c-131">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="5623c-131">Name of resource group.</span></span>

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

### <span data-ttu-id="5623c-132">-Shard</span><span class="sxs-lookup"><span data-stu-id="5623c-132">-Shard</span></span>
<span data-ttu-id="5623c-133">Sharding-Schlüsselpfad.</span><span class="sxs-lookup"><span data-stu-id="5623c-133">Sharding key path.</span></span>

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

### <span data-ttu-id="5623c-134">-Durchsatz</span><span class="sxs-lookup"><span data-stu-id="5623c-134">-Throughput</span></span>
<span data-ttu-id="5623c-135">Der Durchsatz des SQL-Containers (ru/s).</span><span class="sxs-lookup"><span data-stu-id="5623c-135">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="5623c-136">Der Standardwert ist 400.</span><span class="sxs-lookup"><span data-stu-id="5623c-136">Default value is 400.</span></span>

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

### <span data-ttu-id="5623c-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5623c-137">-WhatIf</span></span>
<span data-ttu-id="5623c-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5623c-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5623c-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5623c-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5623c-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5623c-140">CommonParameters</span></span>
<span data-ttu-id="5623c-141">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5623c-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5623c-142">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5623c-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5623c-143">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5623c-143">INPUTS</span></span>

### <span data-ttu-id="5623c-144">Microsoft. Azure. Commands. CosmosDB. Models. PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="5623c-144">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

## <span data-ttu-id="5623c-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5623c-145">OUTPUTS</span></span>

### <span data-ttu-id="5623c-146">Microsoft. Azure. Commands. CosmosDB. Models. PSMongoDBCollectionGetResults</span><span class="sxs-lookup"><span data-stu-id="5623c-146">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

### <span data-ttu-id="5623c-147">Microsoft. Azure. Commands. CosmosDB. Exceptions. ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="5623c-147">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="5623c-148">Notizen</span><span class="sxs-lookup"><span data-stu-id="5623c-148">NOTES</span></span>

## <span data-ttu-id="5623c-149">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5623c-149">RELATED LINKS</span></span>
