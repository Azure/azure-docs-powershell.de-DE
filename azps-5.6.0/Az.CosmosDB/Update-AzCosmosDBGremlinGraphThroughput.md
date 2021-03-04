---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/update-azcosmosdbgremlingraphthroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinGraphThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinGraphThroughput.md
ms.openlocfilehash: c5d7bc79185639c4ec79ab14d7ed2f6201dcedb6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101931275"
---
# <span data-ttu-id="56e30-101">Update-AzCosmosDBGremlinGraphThroughput</span><span class="sxs-lookup"><span data-stu-id="56e30-101">Update-AzCosmosDBGremlinGraphThroughput</span></span>

## <span data-ttu-id="56e30-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="56e30-102">SYNOPSIS</span></span>
<span data-ttu-id="56e30-103">Aktualisiert den Durchsatzwert eines CosmosDB Gremlin Graph.</span><span class="sxs-lookup"><span data-stu-id="56e30-103">Updates the throughput value of a CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="56e30-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="56e30-104">SYNTAX</span></span>

### <span data-ttu-id="56e30-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="56e30-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBGremlinGraphThroughput -DatabaseName <String> [-Name <String>] -ResourceGroupName <String>
 -AccountName <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="56e30-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="56e30-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinGraphThroughput [-Name <String>] -ParentObject <PSGremlinDatabaseGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="56e30-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="56e30-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinGraphThroughput [-Name <String>] -InputObject <PSGremlinGraphGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="56e30-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="56e30-108">DESCRIPTION</span></span>
<span data-ttu-id="56e30-109">Aktualisiert den Durchsatzwert eines CosmosDB Gremlin Graph.</span><span class="sxs-lookup"><span data-stu-id="56e30-109">Updates the throughput value of a CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="56e30-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="56e30-110">EXAMPLES</span></span>

### <span data-ttu-id="56e30-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="56e30-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBGremlinGraphThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -DatabaseName {mydatabaseName} -Name {myGraphName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/gremlinDatabase/{mydatabaseName}/graphs/{myGraphName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="56e30-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="56e30-112">PARAMETERS</span></span>

### <span data-ttu-id="56e30-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="56e30-113">-AccountName</span></span>
<span data-ttu-id="56e30-114">Name des Datenbankkontos "Cosmos DB".</span><span class="sxs-lookup"><span data-stu-id="56e30-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="56e30-115">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="56e30-115">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="56e30-116">Maximaler Durchsatzwert, wenn die automatische Skalierung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="56e30-116">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="56e30-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="56e30-117">-Confirm</span></span>
<span data-ttu-id="56e30-118">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="56e30-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="56e30-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="56e30-119">-DatabaseName</span></span>
<span data-ttu-id="56e30-120">Datenbankname.</span><span class="sxs-lookup"><span data-stu-id="56e30-120">Database name.</span></span>

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

### <span data-ttu-id="56e30-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56e30-121">-DefaultProfile</span></span>
<span data-ttu-id="56e30-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="56e30-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="56e30-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="56e30-123">-InputObject</span></span>
<span data-ttu-id="56e30-124">Gremlin-Datenbankobjekt.</span><span class="sxs-lookup"><span data-stu-id="56e30-124">Gremlin Database object.</span></span>

```yaml
Type: PSGremlinGraphGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="56e30-125">-Name</span><span class="sxs-lookup"><span data-stu-id="56e30-125">-Name</span></span>
<span data-ttu-id="56e30-126">Gremlin Graph Name.</span><span class="sxs-lookup"><span data-stu-id="56e30-126">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="56e30-127">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="56e30-127">-ParentObject</span></span>
<span data-ttu-id="56e30-128">Gremlin-Datenbankobjekt.</span><span class="sxs-lookup"><span data-stu-id="56e30-128">Gremlin Database object.</span></span>

```yaml
Type: PSGremlinDatabaseGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="56e30-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56e30-129">-ResourceGroupName</span></span>
<span data-ttu-id="56e30-130">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="56e30-130">Name of resource group.</span></span>

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

### <span data-ttu-id="56e30-131">-Durchsatz</span><span class="sxs-lookup"><span data-stu-id="56e30-131">-Throughput</span></span>
<span data-ttu-id="56e30-132">Der Durchsatz von Gremlin Graph (RU/s).</span><span class="sxs-lookup"><span data-stu-id="56e30-132">The throughput of Gremlin Graph (RU/s).</span></span>
<span data-ttu-id="56e30-133">Der Standardwert ist 400.</span><span class="sxs-lookup"><span data-stu-id="56e30-133">Default value is 400.</span></span>

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

### <span data-ttu-id="56e30-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="56e30-134">-WhatIf</span></span>
<span data-ttu-id="56e30-135">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="56e30-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="56e30-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="56e30-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="56e30-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56e30-137">CommonParameters</span></span>
<span data-ttu-id="56e30-138">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56e30-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56e30-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="56e30-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56e30-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="56e30-140">INPUTS</span></span>

### <span data-ttu-id="56e30-141">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="56e30-141">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="56e30-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="56e30-142">OUTPUTS</span></span>

### <span data-ttu-id="56e30-143">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="56e30-143">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="56e30-144">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="56e30-144">NOTES</span></span>

## <span data-ttu-id="56e30-145">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="56e30-145">RELATED LINKS</span></span>
