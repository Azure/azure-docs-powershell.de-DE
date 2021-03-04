---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/invoke-azcosmosdbgremlingraphthroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBGremlinGraphThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBGremlinGraphThroughputMigration.md
ms.openlocfilehash: 4fc0c28293484b2f3791145591576d4110ac2974
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101938211"
---
# <span data-ttu-id="923c8-101">Invoke-AzCosmosDBGremlinGraphThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="923c8-101">Invoke-AzCosmosDBGremlinGraphThroughputMigration</span></span>

## <span data-ttu-id="923c8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="923c8-102">SYNOPSIS</span></span>
<span data-ttu-id="923c8-103">Verwenden Sie diese Funktion, um den Durchsatz der automatischen Skalierung in den manuellen Durchsatz zu migrieren und umgekehrt.</span><span class="sxs-lookup"><span data-stu-id="923c8-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="923c8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="923c8-104">SYNTAX</span></span>

### <span data-ttu-id="923c8-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="923c8-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBGremlinGraphThroughputMigration -DatabaseName <String> [-Name <String>]
 -ResourceGroupName <String> -AccountName <String> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="923c8-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="923c8-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBGremlinGraphThroughputMigration [-Name <String>] -ParentObject <PSGremlinDatabaseGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="923c8-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="923c8-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBGremlinGraphThroughputMigration [-Name <String>] -InputObject <PSGremlinGraphGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="923c8-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="923c8-108">DESCRIPTION</span></span>
<span data-ttu-id="923c8-109">ThroughpyteType-Paramter definiert den Durchsatz, zu dem Sie migrieren möchten.</span><span class="sxs-lookup"><span data-stu-id="923c8-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="923c8-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="923c8-110">EXAMPLES</span></span>

### <span data-ttu-id="923c8-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="923c8-111">Example 1</span></span>
```powershell
PS C:\>  $NewGraph =  New-AzCosmosDBGremlinGraph -AccountName myAccountName -ResourceGroupName myRgName -Name myGraphName -Throughput 700 -DatabaseName myDbName
      $AutoscaleThroughput = Invoke-AzCosmosDBGremlinGraphThroughputMigration -InputObject $NewGraph -ThroughputType Autoscale
```

## <span data-ttu-id="923c8-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="923c8-112">PARAMETERS</span></span>

### <span data-ttu-id="923c8-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="923c8-113">-AccountName</span></span>
<span data-ttu-id="923c8-114">Name des Datenbankkontos "Cosmos DB".</span><span class="sxs-lookup"><span data-stu-id="923c8-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="923c8-115">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="923c8-115">-Confirm</span></span>
<span data-ttu-id="923c8-116">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="923c8-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="923c8-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="923c8-117">-DatabaseName</span></span>
<span data-ttu-id="923c8-118">Datenbankname.</span><span class="sxs-lookup"><span data-stu-id="923c8-118">Database name.</span></span>

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

### <span data-ttu-id="923c8-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="923c8-119">-DefaultProfile</span></span>
<span data-ttu-id="923c8-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="923c8-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="923c8-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="923c8-121">-InputObject</span></span>
<span data-ttu-id="923c8-122">Gremlin Graph-Objekt.</span><span class="sxs-lookup"><span data-stu-id="923c8-122">Gremlin Graph object.</span></span>

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

### <span data-ttu-id="923c8-123">-Name</span><span class="sxs-lookup"><span data-stu-id="923c8-123">-Name</span></span>
<span data-ttu-id="923c8-124">Gremlin Graph Name.</span><span class="sxs-lookup"><span data-stu-id="923c8-124">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="923c8-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="923c8-125">-ParentObject</span></span>
<span data-ttu-id="923c8-126">Gremlin-Datenbankobjekt.</span><span class="sxs-lookup"><span data-stu-id="923c8-126">Gremlin Database object.</span></span>

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

### <span data-ttu-id="923c8-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="923c8-127">-ResourceGroupName</span></span>
<span data-ttu-id="923c8-128">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="923c8-128">Name of resource group.</span></span>

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

### <span data-ttu-id="923c8-129">-ThroughputType</span><span class="sxs-lookup"><span data-stu-id="923c8-129">-ThroughputType</span></span>
<span data-ttu-id="923c8-130">Durchsatztyp, zu dem migriert werden soll.</span><span class="sxs-lookup"><span data-stu-id="923c8-130">Throughput type to migrate to.</span></span>
<span data-ttu-id="923c8-131">Mögliche Werte sind: Automatische Skalierung, Manuell.</span><span class="sxs-lookup"><span data-stu-id="923c8-131">Possible values are: Autoscale, Manual.</span></span>

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

### <span data-ttu-id="923c8-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="923c8-132">-WhatIf</span></span>
<span data-ttu-id="923c8-133">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="923c8-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="923c8-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="923c8-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="923c8-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="923c8-135">CommonParameters</span></span>
<span data-ttu-id="923c8-136">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="923c8-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="923c8-137">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="923c8-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="923c8-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="923c8-138">INPUTS</span></span>

### <span data-ttu-id="923c8-139">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="923c8-139">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

### <span data-ttu-id="923c8-140">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="923c8-140">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

## <span data-ttu-id="923c8-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="923c8-141">OUTPUTS</span></span>

### <span data-ttu-id="923c8-142">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="923c8-142">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="923c8-143">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="923c8-143">NOTES</span></span>

## <span data-ttu-id="923c8-144">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="923c8-144">RELATED LINKS</span></span>
