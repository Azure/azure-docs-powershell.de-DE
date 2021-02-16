---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/invoke-azcosmosdbmongodbcollectionthroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBMongoDBCollectionThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBMongoDBCollectionThroughputMigration.md
ms.openlocfilehash: 79dcea6f66d01e9bfa2dd53b990a8f38ec5b0f2a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100171042"
---
# <span data-ttu-id="79a94-101">Invoke-AzCosmosDBMongoDBCollectionThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="79a94-101">Invoke-AzCosmosDBMongoDBCollectionThroughputMigration</span></span>

## <span data-ttu-id="79a94-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="79a94-102">SYNOPSIS</span></span>
<span data-ttu-id="79a94-103">Verwenden Sie diese Funktion, um den Durchsatz der automatischen Skala in den manuellen Durchsatz und umgekehrt zu migrieren.</span><span class="sxs-lookup"><span data-stu-id="79a94-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="79a94-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="79a94-104">SYNTAX</span></span>

### <span data-ttu-id="79a94-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="79a94-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBMongoDBCollectionThroughputMigration -DatabaseName <String> [-Name <String>]
 -ResourceGroupName <String> -AccountName <String> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79a94-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="79a94-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBMongoDBCollectionThroughputMigration [-Name <String>]
 -ParentObject <PSMongoDBDatabaseGetResults> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79a94-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="79a94-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBMongoDBCollectionThroughputMigration [-Name <String>]
 -InputObject <PSMongoDBCollectionGetResults> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="79a94-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="79a94-108">DESCRIPTION</span></span>
<span data-ttu-id="79a94-109">Der ThroughpyteType-Parameterer definiert den Durchsatz, zu dem Sie migrieren möchten.</span><span class="sxs-lookup"><span data-stu-id="79a94-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="79a94-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="79a94-110">EXAMPLES</span></span>

### <span data-ttu-id="79a94-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="79a94-111">Example 1</span></span>
```powershell
PS C:\> $NewCollection =  New-AzCosmosDBMongoDBCollection -AccountName myAccountName -ResourceGroupName myRgName -Name myCollectionName -Throughput  700 -DatabaseName myDbName
      $AutoscaleThroughput = Invoke-AzCosmosDBMongoDBCollectionThroughputMigration -InputObject $NewCollection -ThroughputType Autoscale
```

## <span data-ttu-id="79a94-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="79a94-112">PARAMETERS</span></span>

### <span data-ttu-id="79a94-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="79a94-113">-AccountName</span></span>
<span data-ttu-id="79a94-114">Der Name des Dbdatenbankkontos von Db.</span><span class="sxs-lookup"><span data-stu-id="79a94-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="79a94-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="79a94-115">-Confirm</span></span>
<span data-ttu-id="79a94-116">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="79a94-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="79a94-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="79a94-117">-DatabaseName</span></span>
<span data-ttu-id="79a94-118">Datenbankname.</span><span class="sxs-lookup"><span data-stu-id="79a94-118">Database name.</span></span>

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

### <span data-ttu-id="79a94-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79a94-119">-DefaultProfile</span></span>
<span data-ttu-id="79a94-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="79a94-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="79a94-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="79a94-121">-InputObject</span></span>
<span data-ttu-id="79a94-122">Mongo Collection-Objekt.</span><span class="sxs-lookup"><span data-stu-id="79a94-122">Mongo Collection object.</span></span>

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

### <span data-ttu-id="79a94-123">-Name</span><span class="sxs-lookup"><span data-stu-id="79a94-123">-Name</span></span>
<span data-ttu-id="79a94-124">Sammlungsname.</span><span class="sxs-lookup"><span data-stu-id="79a94-124">Collection name.</span></span>

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

### <span data-ttu-id="79a94-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="79a94-125">-ParentObject</span></span>
<span data-ttu-id="79a94-126">Mongo-Datenbankobjekt.</span><span class="sxs-lookup"><span data-stu-id="79a94-126">Mongo Database object.</span></span>

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

### <span data-ttu-id="79a94-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79a94-127">-ResourceGroupName</span></span>
<span data-ttu-id="79a94-128">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="79a94-128">Name of resource group.</span></span>

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

### <span data-ttu-id="79a94-129">-ThroughputType</span><span class="sxs-lookup"><span data-stu-id="79a94-129">-ThroughputType</span></span>
<span data-ttu-id="79a94-130">Durchsatztyp, zu dem migriert werden soll.</span><span class="sxs-lookup"><span data-stu-id="79a94-130">Throughput type to migrate to.</span></span>
<span data-ttu-id="79a94-131">Mögliche Werte: Autoskalieren, Manuell.</span><span class="sxs-lookup"><span data-stu-id="79a94-131">Possible values are: Autoscale, Manual.</span></span>

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

### <span data-ttu-id="79a94-132">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="79a94-132">-WhatIf</span></span>
<span data-ttu-id="79a94-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="79a94-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="79a94-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="79a94-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="79a94-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79a94-135">CommonParameters</span></span>
<span data-ttu-id="79a94-136">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79a94-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79a94-137">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="79a94-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79a94-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="79a94-138">INPUTS</span></span>

### <span data-ttu-id="79a94-139">Microsoft.Azure.Commands.ExesDB.Models.PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="79a94-139">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

### <span data-ttu-id="79a94-140">Microsoft.Azure.Commands.ExesDB.Models.PSMongoDBCollectionGetResults</span><span class="sxs-lookup"><span data-stu-id="79a94-140">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

## <span data-ttu-id="79a94-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="79a94-141">OUTPUTS</span></span>

### <span data-ttu-id="79a94-142">Microsoft.Azure.Commands.ExesDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="79a94-142">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="79a94-143">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="79a94-143">NOTES</span></span>

## <span data-ttu-id="79a94-144">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="79a94-144">RELATED LINKS</span></span>
