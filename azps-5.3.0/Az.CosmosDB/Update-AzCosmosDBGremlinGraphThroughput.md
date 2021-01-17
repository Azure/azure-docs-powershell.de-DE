---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbgremlingraphthroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinGraphThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinGraphThroughput.md
ms.openlocfilehash: 633ea5263930db74cec3b926c655e54dec10a162
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98470682"
---
# <span data-ttu-id="9a394-101">Update-AzCosmosDBGremlinGraphThroughput</span><span class="sxs-lookup"><span data-stu-id="9a394-101">Update-AzCosmosDBGremlinGraphThroughput</span></span>

## <span data-ttu-id="9a394-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9a394-102">SYNOPSIS</span></span>
<span data-ttu-id="9a394-103">Aktualisiert den Durchsatzwert eines Durchsatzwerts von "Db Gremlin Graph".</span><span class="sxs-lookup"><span data-stu-id="9a394-103">Updates the throughput value of a CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="9a394-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9a394-104">SYNTAX</span></span>

### <span data-ttu-id="9a394-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="9a394-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBGremlinGraphThroughput -DatabaseName <String> [-Name <String>] -ResourceGroupName <String>
 -AccountName <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a394-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9a394-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinGraphThroughput [-Name <String>] -ParentObject <PSGremlinDatabaseGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a394-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9a394-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinGraphThroughput [-Name <String>] -InputObject <PSGremlinGraphGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9a394-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9a394-108">DESCRIPTION</span></span>
<span data-ttu-id="9a394-109">Aktualisiert den Durchsatzwert eines Durchsatzwerts von "Db Gremlin Graph".</span><span class="sxs-lookup"><span data-stu-id="9a394-109">Updates the throughput value of a CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="9a394-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="9a394-110">EXAMPLES</span></span>

### <span data-ttu-id="9a394-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="9a394-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBGremlinGraphThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -DatabaseName {mydatabaseName} -Name {myGraphName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/gremlinDatabase/{mydatabaseName}/graphs/{myGraphName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="9a394-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9a394-112">PARAMETERS</span></span>

### <span data-ttu-id="9a394-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="9a394-113">-AccountName</span></span>
<span data-ttu-id="9a394-114">Name des Dbdatenbankkontos".</span><span class="sxs-lookup"><span data-stu-id="9a394-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="9a394-115">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="9a394-115">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="9a394-116">Der maximale Durchsatzwert, wenn die Automatische Skalierung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="9a394-116">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="9a394-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9a394-117">-Confirm</span></span>
<span data-ttu-id="9a394-118">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9a394-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9a394-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="9a394-119">-DatabaseName</span></span>
<span data-ttu-id="9a394-120">Datenbankname.</span><span class="sxs-lookup"><span data-stu-id="9a394-120">Database name.</span></span>

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

### <span data-ttu-id="9a394-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a394-121">-DefaultProfile</span></span>
<span data-ttu-id="9a394-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9a394-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9a394-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9a394-123">-InputObject</span></span>
<span data-ttu-id="9a394-124">Das Objekt "Gremlin-Datenbank".</span><span class="sxs-lookup"><span data-stu-id="9a394-124">Gremlin Database object.</span></span>

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

### <span data-ttu-id="9a394-125">-Name</span><span class="sxs-lookup"><span data-stu-id="9a394-125">-Name</span></span>
<span data-ttu-id="9a394-126">Name von Gremlin Graph.</span><span class="sxs-lookup"><span data-stu-id="9a394-126">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="9a394-127">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="9a394-127">-ParentObject</span></span>
<span data-ttu-id="9a394-128">Das Objekt "Gremlin-Datenbank".</span><span class="sxs-lookup"><span data-stu-id="9a394-128">Gremlin Database object.</span></span>

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

### <span data-ttu-id="9a394-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a394-129">-ResourceGroupName</span></span>
<span data-ttu-id="9a394-130">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="9a394-130">Name of resource group.</span></span>

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

### <span data-ttu-id="9a394-131">-Throughput</span><span class="sxs-lookup"><span data-stu-id="9a394-131">-Throughput</span></span>
<span data-ttu-id="9a394-132">Der Durchsatz von Gremlin Graph (RU/s).</span><span class="sxs-lookup"><span data-stu-id="9a394-132">The throughput of Gremlin Graph (RU/s).</span></span>
<span data-ttu-id="9a394-133">Der Standardwert ist 400.</span><span class="sxs-lookup"><span data-stu-id="9a394-133">Default value is 400.</span></span>

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

### <span data-ttu-id="9a394-134">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="9a394-134">-WhatIf</span></span>
<span data-ttu-id="9a394-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9a394-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9a394-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9a394-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9a394-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a394-137">CommonParameters</span></span>
<span data-ttu-id="9a394-138">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a394-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a394-139">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9a394-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a394-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="9a394-140">INPUTS</span></span>

### <span data-ttu-id="9a394-141">Microsoft.Azure.Commands.ExesDB.Models.PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="9a394-141">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="9a394-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="9a394-142">OUTPUTS</span></span>

### <span data-ttu-id="9a394-143">Microsoft.Azure.Commands.ExesDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="9a394-143">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="9a394-144">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="9a394-144">NOTES</span></span>

## <span data-ttu-id="9a394-145">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="9a394-145">RELATED LINKS</span></span>
