---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbgremlingraphthroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinGraphThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinGraphThroughput.md
ms.openlocfilehash: 1c29b8fd4f81f67b5eaae9de06d055e5e1a2dace
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100144553"
---
# <span data-ttu-id="25124-101">Get-AzCosmosDBGremlinGraphThroughput</span><span class="sxs-lookup"><span data-stu-id="25124-101">Get-AzCosmosDBGremlinGraphThroughput</span></span>

## <span data-ttu-id="25124-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="25124-102">SYNOPSIS</span></span>
<span data-ttu-id="25124-103">Ruft den Durchsatz eines UnteresDB-Gremlin Graphen ab.</span><span class="sxs-lookup"><span data-stu-id="25124-103">Gets the throughput of a CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="25124-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="25124-104">SYNTAX</span></span>

### <span data-ttu-id="25124-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="25124-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBGremlinGraphThroughput -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="25124-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="25124-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBGremlinGraphThroughput [-Name <String>] -InputObject <PSGremlinGraphGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="25124-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="25124-107">DESCRIPTION</span></span>
<span data-ttu-id="25124-108">Das **Cmdlet "Get-AzCosmosDBGremlinGraphThroughput" (Durchsatz)** ruft den Durchsatz eines Durchsatzes aus DemosDB-Gremlin Graph ab.</span><span class="sxs-lookup"><span data-stu-id="25124-108">The **Get-AzCosmosDBGremlinGraphThroughput** cmdlet gets the throughput of a CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="25124-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="25124-109">EXAMPLES</span></span>

### <span data-ttu-id="25124-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="25124-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBGremlinGraphThroughput -ResourceGroupName {rgName} -AccountName {accountName} -DatabaseName {dbName} -Name {graphName}

Name: {throughputName}
Id: {Id}
Throughput: {value} 
MinimumThroughput: {value}
OfferReplacePending: {value}
```

## <span data-ttu-id="25124-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="25124-111">PARAMETERS</span></span>

### <span data-ttu-id="25124-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="25124-112">-AccountName</span></span>
<span data-ttu-id="25124-113">Der Name des Dbdatenbankkontos von Db.</span><span class="sxs-lookup"><span data-stu-id="25124-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="25124-114">-Confirm</span><span class="sxs-lookup"><span data-stu-id="25124-114">-Confirm</span></span>
<span data-ttu-id="25124-115">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="25124-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="25124-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="25124-116">-DatabaseName</span></span>
<span data-ttu-id="25124-117">Datenbankname.</span><span class="sxs-lookup"><span data-stu-id="25124-117">Database name.</span></span>

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

### <span data-ttu-id="25124-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25124-118">-DefaultProfile</span></span>
<span data-ttu-id="25124-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="25124-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="25124-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="25124-120">-InputObject</span></span>
<span data-ttu-id="25124-121">Gremlin Graph-Objekt.</span><span class="sxs-lookup"><span data-stu-id="25124-121">Gremlin Graph object.</span></span>

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

### <span data-ttu-id="25124-122">-Name</span><span class="sxs-lookup"><span data-stu-id="25124-122">-Name</span></span>
<span data-ttu-id="25124-123">Name von Gremlin Graph.</span><span class="sxs-lookup"><span data-stu-id="25124-123">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="25124-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25124-124">-ResourceGroupName</span></span>
<span data-ttu-id="25124-125">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="25124-125">Name of resource group.</span></span>

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

### <span data-ttu-id="25124-126">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="25124-126">-WhatIf</span></span>
<span data-ttu-id="25124-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="25124-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="25124-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="25124-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="25124-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25124-129">CommonParameters</span></span>
<span data-ttu-id="25124-130">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25124-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25124-131">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="25124-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25124-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="25124-132">INPUTS</span></span>

### <span data-ttu-id="25124-133">Microsoft.Azure.Commands.ExesDB.Models.PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="25124-133">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

## <span data-ttu-id="25124-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="25124-134">OUTPUTS</span></span>

### <span data-ttu-id="25124-135">Microsoft.Azure.Commands.ExesDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="25124-135">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="25124-136">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="25124-136">NOTES</span></span>

## <span data-ttu-id="25124-137">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="25124-137">RELATED LINKS</span></span>
