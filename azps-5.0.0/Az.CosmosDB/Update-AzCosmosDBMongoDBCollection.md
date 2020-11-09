---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbmongodbcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBCollection.md
ms.openlocfilehash: 9440e3541e5022ffbbe328ac81859d2ababa6209
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94299032"
---
# <span data-ttu-id="b5a65-101">Update-AzCosmosDBMongoDBCollection</span><span class="sxs-lookup"><span data-stu-id="b5a65-101">Update-AzCosmosDBMongoDBCollection</span></span>

## <span data-ttu-id="b5a65-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b5a65-102">SYNOPSIS</span></span>
<span data-ttu-id="b5a65-103">Aktualisiert die CosmosDB MongoDB-Sammlung.</span><span class="sxs-lookup"><span data-stu-id="b5a65-103">Updates the CosmosDB MongoDB Collection.</span></span> <span data-ttu-id="b5a65-104">Führt einen clientseitigen Patch-Vorgang durchlesen der vorhandenen Sammlung aus.</span><span class="sxs-lookup"><span data-stu-id="b5a65-104">Performs a client side patch operation by reading the existing Collection.</span></span>

## <span data-ttu-id="b5a65-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b5a65-105">SYNTAX</span></span>

### <span data-ttu-id="b5a65-106">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="b5a65-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBMongoDBCollection -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-Shard <String>]
 [-AnalyticalStorageTtl <Int32>] [-Index <PSMongoIndex[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b5a65-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b5a65-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBCollection [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-Shard <String>] [-AnalyticalStorageTtl <Int32>] [-Index <PSMongoIndex[]>]
 -ParentObject <PSMongoDBDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b5a65-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b5a65-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBCollection [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-Shard <String>] [-AnalyticalStorageTtl <Int32>] [-Index <PSMongoIndex[]>]
 -InputObject <PSMongoDBCollectionGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b5a65-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b5a65-109">DESCRIPTION</span></span>
<span data-ttu-id="b5a65-110">Aktualisiert die CosmosDB MongoDB-Sammlung.</span><span class="sxs-lookup"><span data-stu-id="b5a65-110">Updates the CosmosDB MongoDB Collection.</span></span> <span data-ttu-id="b5a65-111">Führt einen clientseitigen Patch-Vorgang durchlesen der vorhandenen Sammlung aus.</span><span class="sxs-lookup"><span data-stu-id="b5a65-111">Performs a client side patch operation by reading the existing Collection.</span></span>

## <span data-ttu-id="b5a65-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b5a65-112">EXAMPLES</span></span>

### <span data-ttu-id="b5a65-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b5a65-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBMongoDBCollection -AccountName myAccountName -ResourceGroupName myRgName -DatabaseName myDatabaseName -Name myCollectionName -Index $index1,$index2

Name     : collection1
Id       : /subscriptions/mySubId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/mongodbDatabases/myDatabaseName/collect
           ions/myCollectionName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetPropertiesResource
```

## <span data-ttu-id="b5a65-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="b5a65-114">PARAMETERS</span></span>

### <span data-ttu-id="b5a65-115">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="b5a65-115">-AccountName</span></span>
<span data-ttu-id="b5a65-116">Name des Cosmos DB-Daten Bankkontos.</span><span class="sxs-lookup"><span data-stu-id="b5a65-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="b5a65-117">-AnalyticalStorageTtl</span><span class="sxs-lookup"><span data-stu-id="b5a65-117">-AnalyticalStorageTtl</span></span>
<span data-ttu-id="b5a65-118">TTL für Analyse Speicher.</span><span class="sxs-lookup"><span data-stu-id="b5a65-118">TTL for Analytical Storage.</span></span>

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

### <span data-ttu-id="b5a65-119">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="b5a65-119">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="b5a65-120">Maximaler Durchsatz, wenn "AutoScale" aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="b5a65-120">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="b5a65-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b5a65-121">-Confirm</span></span>
<span data-ttu-id="b5a65-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b5a65-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b5a65-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b5a65-123">-DatabaseName</span></span>
<span data-ttu-id="b5a65-124">Datenbankname</span><span class="sxs-lookup"><span data-stu-id="b5a65-124">Database name.</span></span>

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

### <span data-ttu-id="b5a65-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5a65-125">-DefaultProfile</span></span>
<span data-ttu-id="b5a65-126">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b5a65-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b5a65-127">-Index</span><span class="sxs-lookup"><span data-stu-id="b5a65-127">-Index</span></span>
<span data-ttu-id="b5a65-128">Array von PSMongoIndex-Objekten.</span><span class="sxs-lookup"><span data-stu-id="b5a65-128">Array of PSMongoIndex objects.</span></span>

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

### <span data-ttu-id="b5a65-129">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="b5a65-129">-InputObject</span></span>
<span data-ttu-id="b5a65-130">SQL-Container Objekt.</span><span class="sxs-lookup"><span data-stu-id="b5a65-130">Sql Container object.</span></span>

```yaml
Type: PSMongoDBCollectionGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b5a65-131">-Name</span><span class="sxs-lookup"><span data-stu-id="b5a65-131">-Name</span></span>
<span data-ttu-id="b5a65-132">Name der Sammlung.</span><span class="sxs-lookup"><span data-stu-id="b5a65-132">Collection name.</span></span>

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

### <span data-ttu-id="b5a65-133">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="b5a65-133">-ParentObject</span></span>
<span data-ttu-id="b5a65-134">Mongo-Datenbankobjekt</span><span class="sxs-lookup"><span data-stu-id="b5a65-134">Mongo Database object.</span></span>

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

### <span data-ttu-id="b5a65-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5a65-135">-ResourceGroupName</span></span>
<span data-ttu-id="b5a65-136">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="b5a65-136">Name of resource group.</span></span>

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

### <span data-ttu-id="b5a65-137">-Shard</span><span class="sxs-lookup"><span data-stu-id="b5a65-137">-Shard</span></span>
<span data-ttu-id="b5a65-138">Sharding-Schlüsselpfad.</span><span class="sxs-lookup"><span data-stu-id="b5a65-138">Sharding key path.</span></span>

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

### <span data-ttu-id="b5a65-139">-Durchsatz</span><span class="sxs-lookup"><span data-stu-id="b5a65-139">-Throughput</span></span>
<span data-ttu-id="b5a65-140">Der Durchsatz des SQL-Containers (ru/s).</span><span class="sxs-lookup"><span data-stu-id="b5a65-140">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="b5a65-141">Der Standardwert ist 400.</span><span class="sxs-lookup"><span data-stu-id="b5a65-141">Default value is 400.</span></span>

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

### <span data-ttu-id="b5a65-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5a65-142">-WhatIf</span></span>
<span data-ttu-id="b5a65-143">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b5a65-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b5a65-144">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b5a65-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b5a65-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5a65-145">CommonParameters</span></span>
<span data-ttu-id="b5a65-146">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5a65-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5a65-147">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b5a65-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5a65-148">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b5a65-148">INPUTS</span></span>

### <span data-ttu-id="b5a65-149">Microsoft. Azure. Commands. CosmosDB. Models. PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="b5a65-149">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

### <span data-ttu-id="b5a65-150">Microsoft. Azure. Commands. CosmosDB. Models. PSMongoDBCollectionGetResults</span><span class="sxs-lookup"><span data-stu-id="b5a65-150">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

## <span data-ttu-id="b5a65-151">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b5a65-151">OUTPUTS</span></span>

### <span data-ttu-id="b5a65-152">Microsoft. Azure. Commands. CosmosDB. Models. PSMongoDBCollectionGetResults</span><span class="sxs-lookup"><span data-stu-id="b5a65-152">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

### <span data-ttu-id="b5a65-153">Microsoft. Azure. Commands. CosmosDB. Exceptions. ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="b5a65-153">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="b5a65-154">Notizen</span><span class="sxs-lookup"><span data-stu-id="b5a65-154">NOTES</span></span>

## <span data-ttu-id="b5a65-155">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b5a65-155">RELATED LINKS</span></span>
