---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/invoke-azcosmosdbmongodbdatabasethroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBMongoDBDatabaseThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBMongoDBDatabaseThroughputMigration.md
ms.openlocfilehash: 7b30582e0a55e65009fa7248c61cd36f32393249
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100164084"
---
# <span data-ttu-id="cadba-101">Invoke-AzCosmosDBMongoDBDatabaseThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="cadba-101">Invoke-AzCosmosDBMongoDBDatabaseThroughputMigration</span></span>

## <span data-ttu-id="cadba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cadba-102">SYNOPSIS</span></span>
<span data-ttu-id="cadba-103">Verwenden Sie diese Funktion, um den Durchsatz der automatischen Skala in den manuellen Durchsatz und umgekehrt zu migrieren.</span><span class="sxs-lookup"><span data-stu-id="cadba-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="cadba-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cadba-104">SYNTAX</span></span>

### <span data-ttu-id="cadba-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="cadba-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBMongoDBDatabaseThroughputMigration [-Name <String>] -ResourceGroupName <String>
 -AccountName <String> -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cadba-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cadba-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBMongoDBDatabaseThroughputMigration [-Name <String>]
 -ParentObject <PSDatabaseAccountGetResults> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cadba-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cadba-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBMongoDBDatabaseThroughputMigration [-Name <String>] -InputObject <PSMongoDBDatabaseGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cadba-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cadba-108">DESCRIPTION</span></span>
<span data-ttu-id="cadba-109">Der ThroughpyteType-Parameterer definiert den Durchsatz, zu dem Sie migrieren möchten.</span><span class="sxs-lookup"><span data-stu-id="cadba-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="cadba-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="cadba-110">EXAMPLES</span></span>

### <span data-ttu-id="cadba-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="cadba-111">Example 1</span></span>
```powershell
PS C:\>$NewMongodbDatabase =  New-AzCosmosDBMongoDBDatabase -AccountName myAccountName -ResourceGroupName myRgName -Name myDbName -Throughput  700
      $AutoscaleThroughput = Invoke-AzCosmosDBMongoDBDatabaseThroughputMigration -InputObject $NewMongodbDatabase -ThroughputType Autoscale
```

## <span data-ttu-id="cadba-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cadba-112">PARAMETERS</span></span>

### <span data-ttu-id="cadba-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="cadba-113">-AccountName</span></span>
<span data-ttu-id="cadba-114">Der Name des Dbdatenbankkontos von Db.</span><span class="sxs-lookup"><span data-stu-id="cadba-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="cadba-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cadba-115">-Confirm</span></span>
<span data-ttu-id="cadba-116">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="cadba-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cadba-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cadba-117">-DefaultProfile</span></span>
<span data-ttu-id="cadba-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cadba-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cadba-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cadba-119">-InputObject</span></span>
<span data-ttu-id="cadba-120">Mongo-Datenbankobjekt.</span><span class="sxs-lookup"><span data-stu-id="cadba-120">Mongo Database object.</span></span>

```yaml
Type: PSMongoDBDatabaseGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cadba-121">-Name</span><span class="sxs-lookup"><span data-stu-id="cadba-121">-Name</span></span>
<span data-ttu-id="cadba-122">Datenbankname.</span><span class="sxs-lookup"><span data-stu-id="cadba-122">Database name.</span></span>

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

### <span data-ttu-id="cadba-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="cadba-123">-ParentObject</span></span>
<span data-ttu-id="cadba-124">Objekt "Abt.-Konto"</span><span class="sxs-lookup"><span data-stu-id="cadba-124">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccountGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cadba-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cadba-125">-ResourceGroupName</span></span>
<span data-ttu-id="cadba-126">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="cadba-126">Name of resource group.</span></span>

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

### <span data-ttu-id="cadba-127">-ThroughputType</span><span class="sxs-lookup"><span data-stu-id="cadba-127">-ThroughputType</span></span>
<span data-ttu-id="cadba-128">Durchsatztyp, zu dem migriert werden soll.</span><span class="sxs-lookup"><span data-stu-id="cadba-128">Throughput type to migrate to.</span></span>
<span data-ttu-id="cadba-129">Mögliche Werte: Autoskalieren, Manuell.</span><span class="sxs-lookup"><span data-stu-id="cadba-129">Possible values are: Autoscale, Manual.</span></span>

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

### <span data-ttu-id="cadba-130">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="cadba-130">-WhatIf</span></span>
<span data-ttu-id="cadba-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cadba-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cadba-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="cadba-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cadba-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cadba-133">CommonParameters</span></span>
<span data-ttu-id="cadba-134">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cadba-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cadba-135">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cadba-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cadba-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="cadba-136">INPUTS</span></span>

### <span data-ttu-id="cadba-137">Microsoft.Azure.Commands.ExesDB.Models.PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="cadba-137">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

## <span data-ttu-id="cadba-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="cadba-138">OUTPUTS</span></span>

### <span data-ttu-id="cadba-139">Microsoft.Azure.Commands.ExesDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="cadba-139">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="cadba-140">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="cadba-140">NOTES</span></span>

## <span data-ttu-id="cadba-141">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="cadba-141">RELATED LINKS</span></span>
