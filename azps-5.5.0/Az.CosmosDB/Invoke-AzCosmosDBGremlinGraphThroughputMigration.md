---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/invoke-azcosmosdbgremlingraphthroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBGremlinGraphThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBGremlinGraphThroughputMigration.md
ms.openlocfilehash: 16817d4af40ddd27a8838f40618758686af26a58
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100164089"
---
# <span data-ttu-id="2f193-101">Invoke-AzCosmosDBGremlinGraphThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="2f193-101">Invoke-AzCosmosDBGremlinGraphThroughputMigration</span></span>

## <span data-ttu-id="2f193-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2f193-102">SYNOPSIS</span></span>
<span data-ttu-id="2f193-103">Verwenden Sie diese Funktion, um den Durchsatz der automatischen Skala in den manuellen Durchsatz und umgekehrt zu migrieren.</span><span class="sxs-lookup"><span data-stu-id="2f193-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="2f193-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2f193-104">SYNTAX</span></span>

### <span data-ttu-id="2f193-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="2f193-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBGremlinGraphThroughputMigration -DatabaseName <String> [-Name <String>]
 -ResourceGroupName <String> -AccountName <String> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2f193-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2f193-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBGremlinGraphThroughputMigration [-Name <String>] -ParentObject <PSGremlinDatabaseGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2f193-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2f193-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBGremlinGraphThroughputMigration [-Name <String>] -InputObject <PSGremlinGraphGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2f193-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2f193-108">DESCRIPTION</span></span>
<span data-ttu-id="2f193-109">Der ThroughpyteType-Parameterer definiert den Durchsatz, zu dem Sie migrieren möchten.</span><span class="sxs-lookup"><span data-stu-id="2f193-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="2f193-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2f193-110">EXAMPLES</span></span>

### <span data-ttu-id="2f193-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2f193-111">Example 1</span></span>
```powershell
PS C:\>  $NewGraph =  New-AzCosmosDBGremlinGraph -AccountName myAccountName -ResourceGroupName myRgName -Name myGraphName -Throughput 700 -DatabaseName myDbName
      $AutoscaleThroughput = Invoke-AzCosmosDBGremlinGraphThroughputMigration -InputObject $NewGraph -ThroughputType Autoscale
```

## <span data-ttu-id="2f193-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2f193-112">PARAMETERS</span></span>

### <span data-ttu-id="2f193-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="2f193-113">-AccountName</span></span>
<span data-ttu-id="2f193-114">Der Name des Dbdatenbankkontos von Db.</span><span class="sxs-lookup"><span data-stu-id="2f193-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="2f193-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2f193-115">-Confirm</span></span>
<span data-ttu-id="2f193-116">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2f193-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2f193-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="2f193-117">-DatabaseName</span></span>
<span data-ttu-id="2f193-118">Datenbankname.</span><span class="sxs-lookup"><span data-stu-id="2f193-118">Database name.</span></span>

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

### <span data-ttu-id="2f193-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f193-119">-DefaultProfile</span></span>
<span data-ttu-id="2f193-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2f193-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2f193-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2f193-121">-InputObject</span></span>
<span data-ttu-id="2f193-122">Gremlin Graph-Objekt.</span><span class="sxs-lookup"><span data-stu-id="2f193-122">Gremlin Graph object.</span></span>

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

### <span data-ttu-id="2f193-123">-Name</span><span class="sxs-lookup"><span data-stu-id="2f193-123">-Name</span></span>
<span data-ttu-id="2f193-124">Name von Gremlin Graph.</span><span class="sxs-lookup"><span data-stu-id="2f193-124">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="2f193-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="2f193-125">-ParentObject</span></span>
<span data-ttu-id="2f193-126">Das Objekt "Gremlin-Datenbank".</span><span class="sxs-lookup"><span data-stu-id="2f193-126">Gremlin Database object.</span></span>

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

### <span data-ttu-id="2f193-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f193-127">-ResourceGroupName</span></span>
<span data-ttu-id="2f193-128">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="2f193-128">Name of resource group.</span></span>

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

### <span data-ttu-id="2f193-129">-ThroughputType</span><span class="sxs-lookup"><span data-stu-id="2f193-129">-ThroughputType</span></span>
<span data-ttu-id="2f193-130">Durchsatztyp, zu dem migriert werden soll.</span><span class="sxs-lookup"><span data-stu-id="2f193-130">Throughput type to migrate to.</span></span>
<span data-ttu-id="2f193-131">Mögliche Werte: Autoskalieren, Manuell.</span><span class="sxs-lookup"><span data-stu-id="2f193-131">Possible values are: Autoscale, Manual.</span></span>

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

### <span data-ttu-id="2f193-132">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="2f193-132">-WhatIf</span></span>
<span data-ttu-id="2f193-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2f193-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2f193-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2f193-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2f193-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f193-135">CommonParameters</span></span>
<span data-ttu-id="2f193-136">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f193-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f193-137">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2f193-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f193-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2f193-138">INPUTS</span></span>

### <span data-ttu-id="2f193-139">Microsoft.Azure.Commands.ExesDB.Models.PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="2f193-139">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

### <span data-ttu-id="2f193-140">Microsoft.Azure.Commands.ExesDB.Models.PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="2f193-140">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

## <span data-ttu-id="2f193-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2f193-141">OUTPUTS</span></span>

### <span data-ttu-id="2f193-142">Microsoft.Azure.Commands.ExesDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="2f193-142">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="2f193-143">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="2f193-143">NOTES</span></span>

## <span data-ttu-id="2f193-144">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="2f193-144">RELATED LINKS</span></span>
