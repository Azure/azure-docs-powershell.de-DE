---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbmongodbcollectionthroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBCollectionThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBCollectionThroughput.md
ms.openlocfilehash: 0b6b24b0e8c759ca4263d46cf9fe922cd27829e0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98294088"
---
# <span data-ttu-id="6d29c-101">Get-AzCosmosDBMongoDBCollectionThroughput</span><span class="sxs-lookup"><span data-stu-id="6d29c-101">Get-AzCosmosDBMongoDBCollectionThroughput</span></span>

## <span data-ttu-id="6d29c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6d29c-102">SYNOPSIS</span></span>
<span data-ttu-id="6d29c-103">Ruft die Durchsatzeigenschaften von "TongoDB-Sammlung" ab.</span><span class="sxs-lookup"><span data-stu-id="6d29c-103">Gets the CosmosDB throughput properties of MongoDB Collection.</span></span>

## <span data-ttu-id="6d29c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6d29c-104">SYNTAX</span></span>

### <span data-ttu-id="6d29c-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="6d29c-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBMongoDBCollectionThroughput -ResourceGroupName <String> -AccountName <String>
 -DatabaseName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6d29c-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6d29c-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBMongoDBCollectionThroughput [-Name <String>] -InputObject <PSMongoDBCollectionGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6d29c-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6d29c-107">DESCRIPTION</span></span>
<span data-ttu-id="6d29c-108">Das **Cmdlet "Get-AzCosmosDBMongoDBCollectionThroughput"** ruft die Durchsatzeigenschaften der "MongoDB Collection" ab.</span><span class="sxs-lookup"><span data-stu-id="6d29c-108">The **Get-AzCosmosDBMongoDBCollectionThroughput** cmdlet gets the throughput properties of MongoDB Collection.</span></span>

## <span data-ttu-id="6d29c-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6d29c-109">EXAMPLES</span></span>

### <span data-ttu-id="6d29c-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="6d29c-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBMongoDBCollectionThroughput -ResourceGroupName {rgName} -AccountName {accountName} -DatabaseName {databaseName} -Name {collectionName}

Name: {throughputName}
Id: {Id}
Throughput: {value} 
MinimumThroughput: {value}
OfferReplacePending: {value}
```

## <span data-ttu-id="6d29c-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6d29c-111">PARAMETERS</span></span>

### <span data-ttu-id="6d29c-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="6d29c-112">-AccountName</span></span>
<span data-ttu-id="6d29c-113">Name des Dbdatenbankkontos".</span><span class="sxs-lookup"><span data-stu-id="6d29c-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="6d29c-114">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6d29c-114">-Confirm</span></span>
<span data-ttu-id="6d29c-115">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6d29c-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6d29c-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="6d29c-116">-DatabaseName</span></span>
<span data-ttu-id="6d29c-117">Datenbankname.</span><span class="sxs-lookup"><span data-stu-id="6d29c-117">Database name.</span></span>

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

### <span data-ttu-id="6d29c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d29c-118">-DefaultProfile</span></span>
<span data-ttu-id="6d29c-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6d29c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6d29c-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6d29c-120">-InputObject</span></span>
<span data-ttu-id="6d29c-121">Wenn diese Angaben angegeben sind, gibt das Cmdlet die Sammlung mit dem entsprechenden Durchsatzwert zurück.</span><span class="sxs-lookup"><span data-stu-id="6d29c-121">If provided then, the cmdlet returns the collection with the corresponding throughput value.</span></span>

```yaml
Type: PSMongoDBCollectionGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6d29c-122">-Name</span><span class="sxs-lookup"><span data-stu-id="6d29c-122">-Name</span></span>
<span data-ttu-id="6d29c-123">Sammlungsname.</span><span class="sxs-lookup"><span data-stu-id="6d29c-123">Collection name.</span></span>

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

### <span data-ttu-id="6d29c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d29c-124">-ResourceGroupName</span></span>
<span data-ttu-id="6d29c-125">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="6d29c-125">Name of resource group.</span></span>

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

### <span data-ttu-id="6d29c-126">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="6d29c-126">-WhatIf</span></span>
<span data-ttu-id="6d29c-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6d29c-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6d29c-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6d29c-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6d29c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d29c-129">CommonParameters</span></span>
<span data-ttu-id="6d29c-130">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d29c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d29c-131">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6d29c-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d29c-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6d29c-132">INPUTS</span></span>

### <span data-ttu-id="6d29c-133">Microsoft.Azure.Commands.DiesDB.Models.PSMongoDBCollectionGetResults</span><span class="sxs-lookup"><span data-stu-id="6d29c-133">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

## <span data-ttu-id="6d29c-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6d29c-134">OUTPUTS</span></span>

### <span data-ttu-id="6d29c-135">Microsoft.Azure.Commands.ExesDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="6d29c-135">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="6d29c-136">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="6d29c-136">NOTES</span></span>

## <span data-ttu-id="6d29c-137">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="6d29c-137">RELATED LINKS</span></span>
