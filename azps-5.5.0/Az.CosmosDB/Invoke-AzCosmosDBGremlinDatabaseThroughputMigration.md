---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/invoke-azcosmosdbgremlindatabasethroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBGremlinDatabaseThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBGremlinDatabaseThroughputMigration.md
ms.openlocfilehash: 3369415e3c5169695b04ccc8677c3bf0d2f99cd8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100148556"
---
# <span data-ttu-id="0adf5-101">Invoke-AzCosmosDBGremlinDatabaseThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="0adf5-101">Invoke-AzCosmosDBGremlinDatabaseThroughputMigration</span></span>

## <span data-ttu-id="0adf5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0adf5-102">SYNOPSIS</span></span>
<span data-ttu-id="0adf5-103">Verwenden Sie diese Funktion, um den Durchsatz der automatischen Skala in den manuellen Durchsatz und umgekehrt zu migrieren.</span><span class="sxs-lookup"><span data-stu-id="0adf5-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="0adf5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0adf5-104">SYNTAX</span></span>

### <span data-ttu-id="0adf5-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="0adf5-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBGremlinDatabaseThroughputMigration [-Name <String>] -ResourceGroupName <String>
 -AccountName <String> -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0adf5-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0adf5-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBGremlinDatabaseThroughputMigration [-Name <String>]
 -ParentObject <PSDatabaseAccountGetResults> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0adf5-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0adf5-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBGremlinDatabaseThroughputMigration [-Name <String>] -InputObject <PSGremlinDatabaseGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0adf5-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0adf5-108">DESCRIPTION</span></span>
<span data-ttu-id="0adf5-109">Der ThroughpyteType-Parameterer definiert den Durchsatz, zu dem Sie migrieren möchten.</span><span class="sxs-lookup"><span data-stu-id="0adf5-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="0adf5-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0adf5-110">EXAMPLES</span></span>

### <span data-ttu-id="0adf5-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0adf5-111">Example 1</span></span>
```powershell
PS C:\> $NewDb =  New-AzCosmosDBGremlinDatabase -AccountName myAccountName -ResourceGroupName myRgName -Name myDbName -Throughput  700
      $AutoscaleThroughput = Invoke-AzCosmosDBGremlinDatabaseThroughputMigration -InputObject $NewDb -ThroughputType Autoscale
```

## <span data-ttu-id="0adf5-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0adf5-112">PARAMETERS</span></span>

### <span data-ttu-id="0adf5-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="0adf5-113">-AccountName</span></span>
<span data-ttu-id="0adf5-114">Der Name des Dbdatenbankkontos von Db.</span><span class="sxs-lookup"><span data-stu-id="0adf5-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="0adf5-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0adf5-115">-Confirm</span></span>
<span data-ttu-id="0adf5-116">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0adf5-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0adf5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0adf5-117">-DefaultProfile</span></span>
<span data-ttu-id="0adf5-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0adf5-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0adf5-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0adf5-119">-InputObject</span></span>
<span data-ttu-id="0adf5-120">Das Objekt "Gremlin-Datenbank".</span><span class="sxs-lookup"><span data-stu-id="0adf5-120">Gremlin Database object.</span></span>

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

### <span data-ttu-id="0adf5-121">-Name</span><span class="sxs-lookup"><span data-stu-id="0adf5-121">-Name</span></span>
<span data-ttu-id="0adf5-122">Datenbankname.</span><span class="sxs-lookup"><span data-stu-id="0adf5-122">Database name.</span></span>

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

### <span data-ttu-id="0adf5-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="0adf5-123">-ParentObject</span></span>
<span data-ttu-id="0adf5-124">Objekt "Abt.-Konto"</span><span class="sxs-lookup"><span data-stu-id="0adf5-124">CosmosDB Account object</span></span>

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

### <span data-ttu-id="0adf5-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0adf5-125">-ResourceGroupName</span></span>
<span data-ttu-id="0adf5-126">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="0adf5-126">Name of resource group.</span></span>

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

### <span data-ttu-id="0adf5-127">-ThroughputType</span><span class="sxs-lookup"><span data-stu-id="0adf5-127">-ThroughputType</span></span>
<span data-ttu-id="0adf5-128">Durchsatztyp, zu dem migriert werden soll.</span><span class="sxs-lookup"><span data-stu-id="0adf5-128">Throughput type to migrate to.</span></span>
<span data-ttu-id="0adf5-129">Mögliche Werte: Autoskalieren, Manuell.</span><span class="sxs-lookup"><span data-stu-id="0adf5-129">Possible values are: Autoscale, Manual.</span></span>

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

### <span data-ttu-id="0adf5-130">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="0adf5-130">-WhatIf</span></span>
<span data-ttu-id="0adf5-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0adf5-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0adf5-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0adf5-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0adf5-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0adf5-133">CommonParameters</span></span>
<span data-ttu-id="0adf5-134">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0adf5-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0adf5-135">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0adf5-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0adf5-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0adf5-136">INPUTS</span></span>

### <span data-ttu-id="0adf5-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountGetResults</span><span class="sxs-lookup"><span data-stu-id="0adf5-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountGetResults</span></span>

### <span data-ttu-id="0adf5-138">Microsoft.Azure.Commands.ExesDB.Models.PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="0adf5-138">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="0adf5-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0adf5-139">OUTPUTS</span></span>

### <span data-ttu-id="0adf5-140">Microsoft.Azure.Commands.ExesDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="0adf5-140">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="0adf5-141">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="0adf5-141">NOTES</span></span>

## <span data-ttu-id="0adf5-142">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="0adf5-142">RELATED LINKS</span></span>
