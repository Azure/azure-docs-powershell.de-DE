---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbmongodbcollectionthroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBCollectionThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBCollectionThroughput.md
ms.openlocfilehash: 23a88660bd599b0d317b89a1a7c1dbb1e2d51854
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94175281"
---
# <span data-ttu-id="8de5c-101">Update-AzCosmosDBMongoDBCollectionThroughput</span><span class="sxs-lookup"><span data-stu-id="8de5c-101">Update-AzCosmosDBMongoDBCollectionThroughput</span></span>

## <span data-ttu-id="8de5c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8de5c-102">SYNOPSIS</span></span>
<span data-ttu-id="8de5c-103">Aktualisiert den Durchsatz einer CosmosDB-MongoDB-Sammlung.</span><span class="sxs-lookup"><span data-stu-id="8de5c-103">Updates the throughput value of a CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="8de5c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8de5c-104">SYNTAX</span></span>

### <span data-ttu-id="8de5c-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="8de5c-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBMongoDBCollectionThroughput -DatabaseName <String> [-Name <String>]
 -ResourceGroupName <String> -AccountName <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8de5c-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8de5c-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBCollectionThroughput [-Name <String>] -ParentObject <PSMongoDBDatabaseGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8de5c-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8de5c-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBCollectionThroughput [-Name <String>] -InputObject <PSMongoDBCollectionGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8de5c-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8de5c-108">DESCRIPTION</span></span>
<span data-ttu-id="8de5c-109">Aktualisiert den Durchsatz einer CosmosDB-MongoDB-Sammlung.</span><span class="sxs-lookup"><span data-stu-id="8de5c-109">Updates the throughput value of a CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="8de5c-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8de5c-110">EXAMPLES</span></span>

### <span data-ttu-id="8de5c-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8de5c-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBMongoDBCollectionThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -DatabaseName {mydatabaseName} -Name {myCollectionName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/mongodbDatabase/{mydatabaseName}/collections/{myCollectionName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

<span data-ttu-id="8de5c-112">{{Add Example Description here}}</span><span class="sxs-lookup"><span data-stu-id="8de5c-112">{{ Add example description here }}</span></span>

## <span data-ttu-id="8de5c-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="8de5c-113">PARAMETERS</span></span>

### <span data-ttu-id="8de5c-114">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="8de5c-114">-AccountName</span></span>
<span data-ttu-id="8de5c-115">Name des Cosmos DB-Daten Bankkontos.</span><span class="sxs-lookup"><span data-stu-id="8de5c-115">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="8de5c-116">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="8de5c-116">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="8de5c-117">Maximaler Durchsatz, wenn "AutoScale" aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="8de5c-117">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="8de5c-118">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8de5c-118">-Confirm</span></span>
<span data-ttu-id="8de5c-119">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8de5c-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8de5c-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="8de5c-120">-DatabaseName</span></span>
<span data-ttu-id="8de5c-121">Datenbankname</span><span class="sxs-lookup"><span data-stu-id="8de5c-121">Database name.</span></span>

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

### <span data-ttu-id="8de5c-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8de5c-122">-DefaultProfile</span></span>
<span data-ttu-id="8de5c-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8de5c-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8de5c-124">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="8de5c-124">-InputObject</span></span>
<span data-ttu-id="8de5c-125">Mongo-Datenbankobjekt</span><span class="sxs-lookup"><span data-stu-id="8de5c-125">Mongo Database object.</span></span>

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

### <span data-ttu-id="8de5c-126">-Name</span><span class="sxs-lookup"><span data-stu-id="8de5c-126">-Name</span></span>
<span data-ttu-id="8de5c-127">Name der Sammlung.</span><span class="sxs-lookup"><span data-stu-id="8de5c-127">Collection name.</span></span>

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

### <span data-ttu-id="8de5c-128">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="8de5c-128">-ParentObject</span></span>
<span data-ttu-id="8de5c-129">Mongo-Datenbankobjekt</span><span class="sxs-lookup"><span data-stu-id="8de5c-129">Mongo Database object.</span></span>

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

### <span data-ttu-id="8de5c-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8de5c-130">-ResourceGroupName</span></span>
<span data-ttu-id="8de5c-131">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="8de5c-131">Name of resource group.</span></span>

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

### <span data-ttu-id="8de5c-132">-Durchsatz</span><span class="sxs-lookup"><span data-stu-id="8de5c-132">-Throughput</span></span>
<span data-ttu-id="8de5c-133">Der Durchsatz des SQL-Containers (ru/s).</span><span class="sxs-lookup"><span data-stu-id="8de5c-133">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="8de5c-134">Der Standardwert ist 400.</span><span class="sxs-lookup"><span data-stu-id="8de5c-134">Default value is 400.</span></span>

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

### <span data-ttu-id="8de5c-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8de5c-135">-WhatIf</span></span>
<span data-ttu-id="8de5c-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8de5c-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8de5c-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8de5c-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8de5c-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8de5c-138">CommonParameters</span></span>
<span data-ttu-id="8de5c-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8de5c-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8de5c-140">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8de5c-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8de5c-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8de5c-141">INPUTS</span></span>

### <span data-ttu-id="8de5c-142">Microsoft. Azure. Commands. CosmosDB. Models. PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="8de5c-142">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

## <span data-ttu-id="8de5c-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8de5c-143">OUTPUTS</span></span>

### <span data-ttu-id="8de5c-144">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="8de5c-144">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="8de5c-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="8de5c-145">NOTES</span></span>

## <span data-ttu-id="8de5c-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8de5c-146">RELATED LINKS</span></span>
