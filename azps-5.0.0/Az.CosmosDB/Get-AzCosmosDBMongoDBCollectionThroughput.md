---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbmongodbcollectionthroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBCollectionThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBCollectionThroughput.md
ms.openlocfilehash: 0b6b24b0e8c759ca4263d46cf9fe922cd27829e0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94299529"
---
# <span data-ttu-id="0d05a-101">Get-AzCosmosDBMongoDBCollectionThroughput</span><span class="sxs-lookup"><span data-stu-id="0d05a-101">Get-AzCosmosDBMongoDBCollectionThroughput</span></span>

## <span data-ttu-id="0d05a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0d05a-102">SYNOPSIS</span></span>
<span data-ttu-id="0d05a-103">Ruft die CosmosDB-Durchsatz Eigenschaften der MongoDB-Sammlung ab.</span><span class="sxs-lookup"><span data-stu-id="0d05a-103">Gets the CosmosDB throughput properties of MongoDB Collection.</span></span>

## <span data-ttu-id="0d05a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0d05a-104">SYNTAX</span></span>

### <span data-ttu-id="0d05a-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="0d05a-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBMongoDBCollectionThroughput -ResourceGroupName <String> -AccountName <String>
 -DatabaseName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0d05a-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0d05a-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBMongoDBCollectionThroughput [-Name <String>] -InputObject <PSMongoDBCollectionGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0d05a-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0d05a-107">DESCRIPTION</span></span>
<span data-ttu-id="0d05a-108">Das Cmdlet " **Get-AzCosmosDBMongoDBCollectionThroughput** " Ruft die Durchsatz Eigenschaften der MongoDB-Sammlung ab.</span><span class="sxs-lookup"><span data-stu-id="0d05a-108">The **Get-AzCosmosDBMongoDBCollectionThroughput** cmdlet gets the throughput properties of MongoDB Collection.</span></span>

## <span data-ttu-id="0d05a-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0d05a-109">EXAMPLES</span></span>

### <span data-ttu-id="0d05a-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0d05a-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBMongoDBCollectionThroughput -ResourceGroupName {rgName} -AccountName {accountName} -DatabaseName {databaseName} -Name {collectionName}

Name: {throughputName}
Id: {Id}
Throughput: {value} 
MinimumThroughput: {value}
OfferReplacePending: {value}
```

## <span data-ttu-id="0d05a-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="0d05a-111">PARAMETERS</span></span>

### <span data-ttu-id="0d05a-112">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="0d05a-112">-AccountName</span></span>
<span data-ttu-id="0d05a-113">Name des Cosmos DB-Daten Bankkontos.</span><span class="sxs-lookup"><span data-stu-id="0d05a-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="0d05a-114">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0d05a-114">-Confirm</span></span>
<span data-ttu-id="0d05a-115">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0d05a-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0d05a-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="0d05a-116">-DatabaseName</span></span>
<span data-ttu-id="0d05a-117">Datenbankname</span><span class="sxs-lookup"><span data-stu-id="0d05a-117">Database name.</span></span>

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

### <span data-ttu-id="0d05a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d05a-118">-DefaultProfile</span></span>
<span data-ttu-id="0d05a-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0d05a-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0d05a-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="0d05a-120">-InputObject</span></span>
<span data-ttu-id="0d05a-121">Wenn Sie dann bereitgestellt werden, gibt das Cmdlet die Auflistung mit dem entsprechenden Durchsatz zurück.</span><span class="sxs-lookup"><span data-stu-id="0d05a-121">If provided then, the cmdlet returns the collection with the corresponding throughput value.</span></span>

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

### <span data-ttu-id="0d05a-122">-Name</span><span class="sxs-lookup"><span data-stu-id="0d05a-122">-Name</span></span>
<span data-ttu-id="0d05a-123">Name der Sammlung.</span><span class="sxs-lookup"><span data-stu-id="0d05a-123">Collection name.</span></span>

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

### <span data-ttu-id="0d05a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d05a-124">-ResourceGroupName</span></span>
<span data-ttu-id="0d05a-125">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="0d05a-125">Name of resource group.</span></span>

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

### <span data-ttu-id="0d05a-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d05a-126">-WhatIf</span></span>
<span data-ttu-id="0d05a-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0d05a-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0d05a-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0d05a-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0d05a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d05a-129">CommonParameters</span></span>
<span data-ttu-id="0d05a-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d05a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d05a-131">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0d05a-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d05a-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0d05a-132">INPUTS</span></span>

### <span data-ttu-id="0d05a-133">Microsoft. Azure. Commands. CosmosDB. Models. PSMongoDBCollectionGetResults</span><span class="sxs-lookup"><span data-stu-id="0d05a-133">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

## <span data-ttu-id="0d05a-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0d05a-134">OUTPUTS</span></span>

### <span data-ttu-id="0d05a-135">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="0d05a-135">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="0d05a-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="0d05a-136">NOTES</span></span>

## <span data-ttu-id="0d05a-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0d05a-137">RELATED LINKS</span></span>
