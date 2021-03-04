---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/invoke-azcosmosdbgremlindatabasethroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBGremlinDatabaseThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBGremlinDatabaseThroughputMigration.md
ms.openlocfilehash: bbe2cc26eb5f57e31457023285d8f27a1d326321
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101929064"
---
# <span data-ttu-id="24cb7-101">Invoke-AzCosmosDBGremlinDatabaseThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="24cb7-101">Invoke-AzCosmosDBGremlinDatabaseThroughputMigration</span></span>

## <span data-ttu-id="24cb7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="24cb7-102">SYNOPSIS</span></span>
<span data-ttu-id="24cb7-103">Verwenden Sie diese Funktion, um den Durchsatz der automatischen Skalierung in den manuellen Durchsatz zu migrieren und umgekehrt.</span><span class="sxs-lookup"><span data-stu-id="24cb7-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="24cb7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="24cb7-104">SYNTAX</span></span>

### <span data-ttu-id="24cb7-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="24cb7-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBGremlinDatabaseThroughputMigration [-Name <String>] -ResourceGroupName <String>
 -AccountName <String> -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="24cb7-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="24cb7-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBGremlinDatabaseThroughputMigration [-Name <String>]
 -ParentObject <PSDatabaseAccountGetResults> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24cb7-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="24cb7-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBGremlinDatabaseThroughputMigration [-Name <String>] -InputObject <PSGremlinDatabaseGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="24cb7-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="24cb7-108">DESCRIPTION</span></span>
<span data-ttu-id="24cb7-109">ThroughpyteType-Paramter definiert den Durchsatz, zu dem Sie migrieren möchten.</span><span class="sxs-lookup"><span data-stu-id="24cb7-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="24cb7-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="24cb7-110">EXAMPLES</span></span>

### <span data-ttu-id="24cb7-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="24cb7-111">Example 1</span></span>
```powershell
PS C:\> $NewDb =  New-AzCosmosDBGremlinDatabase -AccountName myAccountName -ResourceGroupName myRgName -Name myDbName -Throughput  700
      $AutoscaleThroughput = Invoke-AzCosmosDBGremlinDatabaseThroughputMigration -InputObject $NewDb -ThroughputType Autoscale
```

## <span data-ttu-id="24cb7-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="24cb7-112">PARAMETERS</span></span>

### <span data-ttu-id="24cb7-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="24cb7-113">-AccountName</span></span>
<span data-ttu-id="24cb7-114">Name des Datenbankkontos "Cosmos DB".</span><span class="sxs-lookup"><span data-stu-id="24cb7-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="24cb7-115">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="24cb7-115">-Confirm</span></span>
<span data-ttu-id="24cb7-116">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="24cb7-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24cb7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24cb7-117">-DefaultProfile</span></span>
<span data-ttu-id="24cb7-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="24cb7-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="24cb7-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="24cb7-119">-InputObject</span></span>
<span data-ttu-id="24cb7-120">Gremlin-Datenbankobjekt.</span><span class="sxs-lookup"><span data-stu-id="24cb7-120">Gremlin Database object.</span></span>

```yaml
Type: PSGremlinDatabaseGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="24cb7-121">-Name</span><span class="sxs-lookup"><span data-stu-id="24cb7-121">-Name</span></span>
<span data-ttu-id="24cb7-122">Datenbankname.</span><span class="sxs-lookup"><span data-stu-id="24cb7-122">Database name.</span></span>

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

### <span data-ttu-id="24cb7-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="24cb7-123">-ParentObject</span></span>
<span data-ttu-id="24cb7-124">CosmosDB-Kontoobjekt</span><span class="sxs-lookup"><span data-stu-id="24cb7-124">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccountGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="24cb7-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24cb7-125">-ResourceGroupName</span></span>
<span data-ttu-id="24cb7-126">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="24cb7-126">Name of resource group.</span></span>

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

### <span data-ttu-id="24cb7-127">-ThroughputType</span><span class="sxs-lookup"><span data-stu-id="24cb7-127">-ThroughputType</span></span>
<span data-ttu-id="24cb7-128">Durchsatztyp, zu dem migriert werden soll.</span><span class="sxs-lookup"><span data-stu-id="24cb7-128">Throughput type to migrate to.</span></span>
<span data-ttu-id="24cb7-129">Mögliche Werte sind: Automatische Skalierung, Manuell.</span><span class="sxs-lookup"><span data-stu-id="24cb7-129">Possible values are: Autoscale, Manual.</span></span>

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

### <span data-ttu-id="24cb7-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24cb7-130">-WhatIf</span></span>
<span data-ttu-id="24cb7-131">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="24cb7-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24cb7-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="24cb7-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24cb7-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24cb7-133">CommonParameters</span></span>
<span data-ttu-id="24cb7-134">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24cb7-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24cb7-135">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="24cb7-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24cb7-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="24cb7-136">INPUTS</span></span>

### <span data-ttu-id="24cb7-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountGetResults</span><span class="sxs-lookup"><span data-stu-id="24cb7-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountGetResults</span></span>

### <span data-ttu-id="24cb7-138">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="24cb7-138">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="24cb7-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="24cb7-139">OUTPUTS</span></span>

### <span data-ttu-id="24cb7-140">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="24cb7-140">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="24cb7-141">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="24cb7-141">NOTES</span></span>

## <span data-ttu-id="24cb7-142">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="24cb7-142">RELATED LINKS</span></span>
