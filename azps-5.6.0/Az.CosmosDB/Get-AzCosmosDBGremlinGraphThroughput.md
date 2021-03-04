---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/get-azcosmosdbgremlingraphthroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinGraphThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinGraphThroughput.md
ms.openlocfilehash: f5357e23b8a4e4ec5c613dc7a6b1b0f53e5bac3b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101934424"
---
# <span data-ttu-id="526b0-101">Get-AzCosmosDBGremlinGraphThroughput</span><span class="sxs-lookup"><span data-stu-id="526b0-101">Get-AzCosmosDBGremlinGraphThroughput</span></span>

## <span data-ttu-id="526b0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="526b0-102">SYNOPSIS</span></span>
<span data-ttu-id="526b0-103">Ruft den Durchsatz eines CosmosDB Gremlin Graph ab.</span><span class="sxs-lookup"><span data-stu-id="526b0-103">Gets the throughput of a CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="526b0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="526b0-104">SYNTAX</span></span>

### <span data-ttu-id="526b0-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="526b0-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBGremlinGraphThroughput -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="526b0-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="526b0-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBGremlinGraphThroughput [-Name <String>] -InputObject <PSGremlinGraphGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="526b0-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="526b0-107">DESCRIPTION</span></span>
<span data-ttu-id="526b0-108">Das **Cmdlet Get-AzCosmosDBGremlinGraphThroughput** ruft den Durchsatz eines CosmosDB Gremlin Graph ab.</span><span class="sxs-lookup"><span data-stu-id="526b0-108">The **Get-AzCosmosDBGremlinGraphThroughput** cmdlet gets the throughput of a CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="526b0-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="526b0-109">EXAMPLES</span></span>

### <span data-ttu-id="526b0-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="526b0-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBGremlinGraphThroughput -ResourceGroupName {rgName} -AccountName {accountName} -DatabaseName {dbName} -Name {graphName}

Name: {throughputName}
Id: {Id}
Throughput: {value} 
MinimumThroughput: {value}
OfferReplacePending: {value}
```

## <span data-ttu-id="526b0-111">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="526b0-111">PARAMETERS</span></span>

### <span data-ttu-id="526b0-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="526b0-112">-AccountName</span></span>
<span data-ttu-id="526b0-113">Name des Datenbankkontos "Cosmos DB".</span><span class="sxs-lookup"><span data-stu-id="526b0-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="526b0-114">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="526b0-114">-Confirm</span></span>
<span data-ttu-id="526b0-115">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="526b0-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="526b0-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="526b0-116">-DatabaseName</span></span>
<span data-ttu-id="526b0-117">Datenbankname.</span><span class="sxs-lookup"><span data-stu-id="526b0-117">Database name.</span></span>

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

### <span data-ttu-id="526b0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="526b0-118">-DefaultProfile</span></span>
<span data-ttu-id="526b0-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="526b0-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="526b0-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="526b0-120">-InputObject</span></span>
<span data-ttu-id="526b0-121">Gremlin Graph-Objekt.</span><span class="sxs-lookup"><span data-stu-id="526b0-121">Gremlin Graph object.</span></span>

```yaml
Type: PSGremlinGraphGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="526b0-122">-Name</span><span class="sxs-lookup"><span data-stu-id="526b0-122">-Name</span></span>
<span data-ttu-id="526b0-123">Gremlin Graph Name.</span><span class="sxs-lookup"><span data-stu-id="526b0-123">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="526b0-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="526b0-124">-ResourceGroupName</span></span>
<span data-ttu-id="526b0-125">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="526b0-125">Name of resource group.</span></span>

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

### <span data-ttu-id="526b0-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="526b0-126">-WhatIf</span></span>
<span data-ttu-id="526b0-127">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="526b0-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="526b0-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="526b0-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="526b0-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="526b0-129">CommonParameters</span></span>
<span data-ttu-id="526b0-130">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="526b0-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="526b0-131">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="526b0-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="526b0-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="526b0-132">INPUTS</span></span>

### <span data-ttu-id="526b0-133">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="526b0-133">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

## <span data-ttu-id="526b0-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="526b0-134">OUTPUTS</span></span>

### <span data-ttu-id="526b0-135">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="526b0-135">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="526b0-136">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="526b0-136">NOTES</span></span>

## <span data-ttu-id="526b0-137">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="526b0-137">RELATED LINKS</span></span>
