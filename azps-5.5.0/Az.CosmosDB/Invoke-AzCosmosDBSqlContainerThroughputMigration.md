---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/invoke-azcosmosdbsqlcontainerthroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBSqlContainerThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBSqlContainerThroughputMigration.md
ms.openlocfilehash: ac15f6ba4d8db1e4f3ab35c34b33b78fdefa05a3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100144548"
---
# <span data-ttu-id="6e03f-101">Invoke-AzCosmosDBSqlContainerThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="6e03f-101">Invoke-AzCosmosDBSqlContainerThroughputMigration</span></span>

## <span data-ttu-id="6e03f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6e03f-102">SYNOPSIS</span></span>
<span data-ttu-id="6e03f-103">Verwenden Sie diese Funktion, um den Durchsatz der automatischen Skala in den manuellen Durchsatz und umgekehrt zu migrieren.</span><span class="sxs-lookup"><span data-stu-id="6e03f-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="6e03f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6e03f-104">SYNTAX</span></span>

### <span data-ttu-id="6e03f-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="6e03f-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBSqlContainerThroughputMigration -DatabaseName <String> [-Name <String>]
 -ResourceGroupName <String> -AccountName <String> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6e03f-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6e03f-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBSqlContainerThroughputMigration [-Name <String>] -ParentObject <PSSqlDatabaseGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6e03f-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6e03f-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBSqlContainerThroughputMigration [-Name <String>] -InputObject <PSSqlContainerGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6e03f-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6e03f-108">DESCRIPTION</span></span>
<span data-ttu-id="6e03f-109">Der ThroughpyteType-Parameterer definiert den Durchsatz, zu dem Sie migrieren möchten.</span><span class="sxs-lookup"><span data-stu-id="6e03f-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="6e03f-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6e03f-110">EXAMPLES</span></span>

### <span data-ttu-id="6e03f-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="6e03f-111">Example 1</span></span>
```powershell
PS C:\>$NewSqlContainer =  New-AzCosmosDBSqlContainer -AccountName myAccountName -ResourceGroupName myRgName -Name myContainerName  -Throughput  700 -DatabaseName myDbName
      $AutoscaleThroughput = Invoke-AzCosmosDBSqlContainerThroughputMigration -InputObject $NewSqlContainer -ThroughputType Autoscale
```

## <span data-ttu-id="6e03f-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6e03f-112">PARAMETERS</span></span>

### <span data-ttu-id="6e03f-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="6e03f-113">-AccountName</span></span>
<span data-ttu-id="6e03f-114">Der Name des Dbdatenbankkontos von Db.</span><span class="sxs-lookup"><span data-stu-id="6e03f-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="6e03f-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6e03f-115">-Confirm</span></span>
<span data-ttu-id="6e03f-116">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6e03f-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6e03f-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="6e03f-117">-DatabaseName</span></span>
<span data-ttu-id="6e03f-118">Datenbankname.</span><span class="sxs-lookup"><span data-stu-id="6e03f-118">Database name.</span></span>

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

### <span data-ttu-id="6e03f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e03f-119">-DefaultProfile</span></span>
<span data-ttu-id="6e03f-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6e03f-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6e03f-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6e03f-121">-InputObject</span></span>
<span data-ttu-id="6e03f-122">Sql Container-Objekt.</span><span class="sxs-lookup"><span data-stu-id="6e03f-122">Sql Container object.</span></span>

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

### <span data-ttu-id="6e03f-123">-Name</span><span class="sxs-lookup"><span data-stu-id="6e03f-123">-Name</span></span>
<span data-ttu-id="6e03f-124">Containername.</span><span class="sxs-lookup"><span data-stu-id="6e03f-124">Container name.</span></span>

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

### <span data-ttu-id="6e03f-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="6e03f-125">-ParentObject</span></span>
<span data-ttu-id="6e03f-126">Sql-Datenbankobjekt.</span><span class="sxs-lookup"><span data-stu-id="6e03f-126">Sql Database object.</span></span>

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

### <span data-ttu-id="6e03f-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e03f-127">-ResourceGroupName</span></span>
<span data-ttu-id="6e03f-128">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="6e03f-128">Name of resource group.</span></span>

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

### <span data-ttu-id="6e03f-129">-ThroughputType</span><span class="sxs-lookup"><span data-stu-id="6e03f-129">-ThroughputType</span></span>
<span data-ttu-id="6e03f-130">Durchsatztyp, zu dem migriert werden soll.</span><span class="sxs-lookup"><span data-stu-id="6e03f-130">Throughput type to migrate to.</span></span>
<span data-ttu-id="6e03f-131">Mögliche Werte: Autoskalieren, Manuell.</span><span class="sxs-lookup"><span data-stu-id="6e03f-131">Possible values are: Autoscale, Manual.</span></span>

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

### <span data-ttu-id="6e03f-132">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="6e03f-132">-WhatIf</span></span>
<span data-ttu-id="6e03f-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6e03f-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6e03f-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6e03f-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6e03f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e03f-135">CommonParameters</span></span>
<span data-ttu-id="6e03f-136">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e03f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e03f-137">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6e03f-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e03f-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6e03f-138">INPUTS</span></span>

### <span data-ttu-id="6e03f-139">Microsoft.Azure.Commands.ExesDB.Models.PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="6e03f-139">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="6e03f-140">Microsoft.Azure.Commands.ExesDB.Models.PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="6e03f-140">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

## <span data-ttu-id="6e03f-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6e03f-141">OUTPUTS</span></span>

### <span data-ttu-id="6e03f-142">Microsoft.Azure.Commands.ExesDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="6e03f-142">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="6e03f-143">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="6e03f-143">NOTES</span></span>

## <span data-ttu-id="6e03f-144">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="6e03f-144">RELATED LINKS</span></span>
