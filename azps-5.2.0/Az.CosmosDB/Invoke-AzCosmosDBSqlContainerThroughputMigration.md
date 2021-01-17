---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/invoke-azcosmosdbsqlcontainerthroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBSqlContainerThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBSqlContainerThroughputMigration.md
ms.openlocfilehash: 61b564e8b92193b873e815b4a65f7c009dabf0f6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98361232"
---
# <span data-ttu-id="e7a06-101">Invoke-AzCosmosDBSqlContainerThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="e7a06-101">Invoke-AzCosmosDBSqlContainerThroughputMigration</span></span>

## <span data-ttu-id="e7a06-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e7a06-102">SYNOPSIS</span></span>
<span data-ttu-id="e7a06-103">Verwenden Sie diese Funktion, um den Durchsatz der automatischen Skala in den manuellen Durchsatz und umgekehrt zu migrieren.</span><span class="sxs-lookup"><span data-stu-id="e7a06-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="e7a06-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e7a06-104">SYNTAX</span></span>

### <span data-ttu-id="e7a06-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="e7a06-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBSqlContainerThroughputMigration -DatabaseName <String> [-Name <String>]
 -ResourceGroupName <String> -AccountName <String> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e7a06-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e7a06-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBSqlContainerThroughputMigration [-Name <String>] -ParentObject <PSSqlDatabaseGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e7a06-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e7a06-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBSqlContainerThroughputMigration [-Name <String>] -InputObject <PSSqlContainerGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e7a06-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e7a06-108">DESCRIPTION</span></span>
<span data-ttu-id="e7a06-109">Der ThroughpyteType-Parameterer definiert den Durchsatz, zu dem Sie migrieren möchten.</span><span class="sxs-lookup"><span data-stu-id="e7a06-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="e7a06-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e7a06-110">EXAMPLES</span></span>

### <span data-ttu-id="e7a06-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e7a06-111">Example 1</span></span>
```powershell
PS C:\>$NewSqlContainer =  New-AzCosmosDBSqlContainer -AccountName myAccountName -ResourceGroupName myRgName -Name myContainerName  -Throughput  700 -DatabaseName myDbName
      $AutoscaleThroughput = Invoke-AzCosmosDBSqlContainerThroughputMigration -InputObject $NewSqlContainer -ThroughputType Autoscale
```


## <span data-ttu-id="e7a06-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e7a06-112">PARAMETERS</span></span>

### <span data-ttu-id="e7a06-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="e7a06-113">-AccountName</span></span>
<span data-ttu-id="e7a06-114">Der Name des Dbdatenbankkontos von Db.</span><span class="sxs-lookup"><span data-stu-id="e7a06-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="e7a06-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e7a06-115">-Confirm</span></span>
<span data-ttu-id="e7a06-116">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e7a06-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e7a06-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e7a06-117">-DatabaseName</span></span>
<span data-ttu-id="e7a06-118">Datenbankname.</span><span class="sxs-lookup"><span data-stu-id="e7a06-118">Database name.</span></span>

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

### <span data-ttu-id="e7a06-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7a06-119">-DefaultProfile</span></span>
<span data-ttu-id="e7a06-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e7a06-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e7a06-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e7a06-121">-InputObject</span></span>
<span data-ttu-id="e7a06-122">Sql Container-Objekt.</span><span class="sxs-lookup"><span data-stu-id="e7a06-122">Sql Container object.</span></span>

```yaml
Type: PSSqlContainerGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e7a06-123">-Name</span><span class="sxs-lookup"><span data-stu-id="e7a06-123">-Name</span></span>
<span data-ttu-id="e7a06-124">Containername.</span><span class="sxs-lookup"><span data-stu-id="e7a06-124">Container name.</span></span>

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

### <span data-ttu-id="e7a06-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="e7a06-125">-ParentObject</span></span>
<span data-ttu-id="e7a06-126">Sql-Datenbankobjekt.</span><span class="sxs-lookup"><span data-stu-id="e7a06-126">Sql Database object.</span></span>

```yaml
Type: PSSqlDatabaseGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e7a06-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7a06-127">-ResourceGroupName</span></span>
<span data-ttu-id="e7a06-128">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="e7a06-128">Name of resource group.</span></span>

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

### <span data-ttu-id="e7a06-129">-ThroughputType</span><span class="sxs-lookup"><span data-stu-id="e7a06-129">-ThroughputType</span></span>
<span data-ttu-id="e7a06-130">Durchsatztyp, zu dem migriert werden soll.</span><span class="sxs-lookup"><span data-stu-id="e7a06-130">Throughput type to migrate to.</span></span>
<span data-ttu-id="e7a06-131">Mögliche Werte: Autoskalieren, Manuell.</span><span class="sxs-lookup"><span data-stu-id="e7a06-131">Possible values are: Autoscale, Manual.</span></span>

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

### <span data-ttu-id="e7a06-132">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="e7a06-132">-WhatIf</span></span>
<span data-ttu-id="e7a06-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e7a06-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e7a06-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e7a06-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e7a06-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7a06-135">CommonParameters</span></span>
<span data-ttu-id="e7a06-136">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7a06-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7a06-137">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e7a06-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7a06-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e7a06-138">INPUTS</span></span>

### <span data-ttu-id="e7a06-139">Microsoft.Azure.Commands.ExesDB.Models.PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="e7a06-139">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="e7a06-140">Microsoft.Azure.Commands.ExesDB.Models.PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="e7a06-140">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

## <span data-ttu-id="e7a06-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e7a06-141">OUTPUTS</span></span>

### <span data-ttu-id="e7a06-142">Microsoft.Azure.Commands.DiesDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="e7a06-142">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="e7a06-143">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="e7a06-143">NOTES</span></span>

## <span data-ttu-id="e7a06-144">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="e7a06-144">RELATED LINKS</span></span>
