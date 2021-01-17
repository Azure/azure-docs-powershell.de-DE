---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/invoke-azcosmosdbsqldatabasethroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBSqlDatabaseThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBSqlDatabaseThroughputMigration.md
ms.openlocfilehash: 927cdbd6c599b090a66120e95a1ac1a024360271
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98472835"
---
# <span data-ttu-id="7bec6-101">Invoke-AzCosmosDBSqlDatabaseThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="7bec6-101">Invoke-AzCosmosDBSqlDatabaseThroughputMigration</span></span>

## <span data-ttu-id="7bec6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7bec6-102">SYNOPSIS</span></span>
<span data-ttu-id="7bec6-103">Verwenden Sie diese Funktion, um den Durchsatz der automatischen Skala in den manuellen Durchsatz und umgekehrt zu migrieren.</span><span class="sxs-lookup"><span data-stu-id="7bec6-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="7bec6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7bec6-104">SYNTAX</span></span>

### <span data-ttu-id="7bec6-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="7bec6-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBSqlDatabaseThroughputMigration [-Name <String>] -ResourceGroupName <String>
 -AccountName <String> -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7bec6-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7bec6-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBSqlDatabaseThroughputMigration [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7bec6-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7bec6-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBSqlDatabaseThroughputMigration [-Name <String>] -InputObject <PSSqlDatabaseGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7bec6-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7bec6-108">DESCRIPTION</span></span>
<span data-ttu-id="7bec6-109">Der ThroughpyteType-Parameterer definiert den Durchsatz, zu dem Sie migrieren möchten.</span><span class="sxs-lookup"><span data-stu-id="7bec6-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="7bec6-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="7bec6-110">EXAMPLES</span></span>

### <span data-ttu-id="7bec6-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="7bec6-111">Example 1</span></span>
```powershell
PS C:\> $NewSqlDatabase =  New-AzCosmosDBSqlDatabase -AccountName myAccountName -ResourceGroupName myRgName -Name myDbName -Throughput  700
      $AutoscaleThroughput = Invoke-AzCosmosDBSqlDatabaseThroughputMigration -InputObject $NewSqlDatabase -ThroughputType Autoscale
```


## <span data-ttu-id="7bec6-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7bec6-112">PARAMETERS</span></span>

### <span data-ttu-id="7bec6-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="7bec6-113">-AccountName</span></span>
<span data-ttu-id="7bec6-114">Name des Dbdatenbankkontos".</span><span class="sxs-lookup"><span data-stu-id="7bec6-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="7bec6-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7bec6-115">-Confirm</span></span>
<span data-ttu-id="7bec6-116">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7bec6-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7bec6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7bec6-117">-DefaultProfile</span></span>
<span data-ttu-id="7bec6-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7bec6-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7bec6-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7bec6-119">-InputObject</span></span>
<span data-ttu-id="7bec6-120">Sql-Datenbankobjekt.</span><span class="sxs-lookup"><span data-stu-id="7bec6-120">Sql Database object.</span></span>

```yaml
Type: PSSqlDatabaseGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7bec6-121">-Name</span><span class="sxs-lookup"><span data-stu-id="7bec6-121">-Name</span></span>
<span data-ttu-id="7bec6-122">Datenbankname.</span><span class="sxs-lookup"><span data-stu-id="7bec6-122">Database name.</span></span>

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

### <span data-ttu-id="7bec6-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="7bec6-123">-ParentObject</span></span>
<span data-ttu-id="7bec6-124">Objekt "Abt.-Konto"</span><span class="sxs-lookup"><span data-stu-id="7bec6-124">CosmosDB Account object</span></span>

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

### <span data-ttu-id="7bec6-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7bec6-125">-ResourceGroupName</span></span>
<span data-ttu-id="7bec6-126">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="7bec6-126">Name of resource group.</span></span>

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

### <span data-ttu-id="7bec6-127">-ThroughputType</span><span class="sxs-lookup"><span data-stu-id="7bec6-127">-ThroughputType</span></span>
<span data-ttu-id="7bec6-128">Durchsatztyp, zu dem migriert werden soll.</span><span class="sxs-lookup"><span data-stu-id="7bec6-128">Throughput type to migrate to.</span></span>
<span data-ttu-id="7bec6-129">Mögliche Werte sind: Autoskalieren, Manuell.</span><span class="sxs-lookup"><span data-stu-id="7bec6-129">Possible values are: Autoscale, Manual.</span></span>

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

### <span data-ttu-id="7bec6-130">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="7bec6-130">-WhatIf</span></span>
<span data-ttu-id="7bec6-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7bec6-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7bec6-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7bec6-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7bec6-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7bec6-133">CommonParameters</span></span>
<span data-ttu-id="7bec6-134">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7bec6-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7bec6-135">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7bec6-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7bec6-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="7bec6-136">INPUTS</span></span>

### <span data-ttu-id="7bec6-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountGetResults</span><span class="sxs-lookup"><span data-stu-id="7bec6-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountGetResults</span></span>

### <span data-ttu-id="7bec6-138">Microsoft.Azure.Commands.ExesDB.Models.PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="7bec6-138">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

## <span data-ttu-id="7bec6-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="7bec6-139">OUTPUTS</span></span>

### <span data-ttu-id="7bec6-140">Microsoft.Azure.Commands.DiesDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="7bec6-140">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="7bec6-141">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="7bec6-141">NOTES</span></span>

## <span data-ttu-id="7bec6-142">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="7bec6-142">RELATED LINKS</span></span>
