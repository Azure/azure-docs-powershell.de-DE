---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/invoke-azcosmosdbmongodbcollectionthroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBMongoDBCollectionThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBMongoDBCollectionThroughputMigration.md
ms.openlocfilehash: 230fb5f43bceda32489ac632cb995eb5e4adac25
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101928651"
---
# <span data-ttu-id="3f55a-101">Invoke-AzCosmosDBMongoDBCollectionThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="3f55a-101">Invoke-AzCosmosDBMongoDBCollectionThroughputMigration</span></span>

## <span data-ttu-id="3f55a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3f55a-102">SYNOPSIS</span></span>
<span data-ttu-id="3f55a-103">Verwenden Sie diese Funktion, um den Durchsatz der automatischen Skalierung in den manuellen Durchsatz zu migrieren und umgekehrt.</span><span class="sxs-lookup"><span data-stu-id="3f55a-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="3f55a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3f55a-104">SYNTAX</span></span>

### <span data-ttu-id="3f55a-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="3f55a-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBMongoDBCollectionThroughputMigration -DatabaseName <String> [-Name <String>]
 -ResourceGroupName <String> -AccountName <String> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3f55a-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3f55a-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBMongoDBCollectionThroughputMigration [-Name <String>]
 -ParentObject <PSMongoDBDatabaseGetResults> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3f55a-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3f55a-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBMongoDBCollectionThroughputMigration [-Name <String>]
 -InputObject <PSMongoDBCollectionGetResults> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3f55a-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3f55a-108">DESCRIPTION</span></span>
<span data-ttu-id="3f55a-109">ThroughpyteType-Paramter definiert den Durchsatz, zu dem Sie migrieren möchten.</span><span class="sxs-lookup"><span data-stu-id="3f55a-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="3f55a-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3f55a-110">EXAMPLES</span></span>

### <span data-ttu-id="3f55a-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="3f55a-111">Example 1</span></span>
```powershell
PS C:\> $NewCollection =  New-AzCosmosDBMongoDBCollection -AccountName myAccountName -ResourceGroupName myRgName -Name myCollectionName -Throughput  700 -DatabaseName myDbName
      $AutoscaleThroughput = Invoke-AzCosmosDBMongoDBCollectionThroughputMigration -InputObject $NewCollection -ThroughputType Autoscale
```

## <span data-ttu-id="3f55a-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="3f55a-112">PARAMETERS</span></span>

### <span data-ttu-id="3f55a-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="3f55a-113">-AccountName</span></span>
<span data-ttu-id="3f55a-114">Name des Datenbankkontos "Cosmos DB".</span><span class="sxs-lookup"><span data-stu-id="3f55a-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="3f55a-115">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3f55a-115">-Confirm</span></span>
<span data-ttu-id="3f55a-116">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3f55a-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3f55a-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="3f55a-117">-DatabaseName</span></span>
<span data-ttu-id="3f55a-118">Datenbankname.</span><span class="sxs-lookup"><span data-stu-id="3f55a-118">Database name.</span></span>

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

### <span data-ttu-id="3f55a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f55a-119">-DefaultProfile</span></span>
<span data-ttu-id="3f55a-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3f55a-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3f55a-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3f55a-121">-InputObject</span></span>
<span data-ttu-id="3f55a-122">Mongo Collection-Objekt.</span><span class="sxs-lookup"><span data-stu-id="3f55a-122">Mongo Collection object.</span></span>

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

### <span data-ttu-id="3f55a-123">-Name</span><span class="sxs-lookup"><span data-stu-id="3f55a-123">-Name</span></span>
<span data-ttu-id="3f55a-124">Sammlungsname.</span><span class="sxs-lookup"><span data-stu-id="3f55a-124">Collection name.</span></span>

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

### <span data-ttu-id="3f55a-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="3f55a-125">-ParentObject</span></span>
<span data-ttu-id="3f55a-126">Mongo-Datenbankobjekt.</span><span class="sxs-lookup"><span data-stu-id="3f55a-126">Mongo Database object.</span></span>

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

### <span data-ttu-id="3f55a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f55a-127">-ResourceGroupName</span></span>
<span data-ttu-id="3f55a-128">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="3f55a-128">Name of resource group.</span></span>

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

### <span data-ttu-id="3f55a-129">-ThroughputType</span><span class="sxs-lookup"><span data-stu-id="3f55a-129">-ThroughputType</span></span>
<span data-ttu-id="3f55a-130">Durchsatztyp, zu dem migriert werden soll.</span><span class="sxs-lookup"><span data-stu-id="3f55a-130">Throughput type to migrate to.</span></span>
<span data-ttu-id="3f55a-131">Mögliche Werte sind: Automatische Skalierung, Manuell.</span><span class="sxs-lookup"><span data-stu-id="3f55a-131">Possible values are: Autoscale, Manual.</span></span>

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

### <span data-ttu-id="3f55a-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3f55a-132">-WhatIf</span></span>
<span data-ttu-id="3f55a-133">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3f55a-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3f55a-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3f55a-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3f55a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f55a-135">CommonParameters</span></span>
<span data-ttu-id="3f55a-136">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f55a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f55a-137">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3f55a-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f55a-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3f55a-138">INPUTS</span></span>

### <span data-ttu-id="3f55a-139">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="3f55a-139">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

### <span data-ttu-id="3f55a-140">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span><span class="sxs-lookup"><span data-stu-id="3f55a-140">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

## <span data-ttu-id="3f55a-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3f55a-141">OUTPUTS</span></span>

### <span data-ttu-id="3f55a-142">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="3f55a-142">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="3f55a-143">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="3f55a-143">NOTES</span></span>

## <span data-ttu-id="3f55a-144">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="3f55a-144">RELATED LINKS</span></span>
