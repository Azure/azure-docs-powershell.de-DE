---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlDatabase.md
ms.openlocfilehash: 2953da3747404c0b6b98992cc8a8b80573da5129
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100175793"
---
# <span data-ttu-id="159ca-101">New-AzCosmosDBSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="159ca-101">New-AzCosmosDBSqlDatabase</span></span>

## <span data-ttu-id="159ca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="159ca-102">SYNOPSIS</span></span>
<span data-ttu-id="159ca-103">Erstellt eine neue Sql-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="159ca-103">Creates a new CosmosDB Sql Database.</span></span>

## <span data-ttu-id="159ca-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="159ca-104">SYNTAX</span></span>

### <span data-ttu-id="159ca-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="159ca-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBSqlDatabase -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="159ca-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="159ca-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBSqlDatabase -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="159ca-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="159ca-107">DESCRIPTION</span></span>
<span data-ttu-id="159ca-108">Erstellt eine neue Sql-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="159ca-108">Creates a new CosmosDB Sql Database.</span></span>

## <span data-ttu-id="159ca-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="159ca-109">EXAMPLES</span></span>

### <span data-ttu-id="159ca-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="159ca-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlDatabase -AccountName myAccountName -Name myDatabaseName -ResourceGroupName myResourcegroupName

Name     : myDatabaseName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/sqlDatabases/myDatabaseName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetPropertiesResource
```

## <span data-ttu-id="159ca-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="159ca-111">PARAMETERS</span></span>

### <span data-ttu-id="159ca-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="159ca-112">-AccountName</span></span>
<span data-ttu-id="159ca-113">Der Name des Dbdatenbankkontos von Db.</span><span class="sxs-lookup"><span data-stu-id="159ca-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="159ca-114">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="159ca-114">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="159ca-115">Der maximale Durchsatzwert, wenn die Automatische Skalierung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="159ca-115">Maximum Throughput value if autoscale is enabled.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="159ca-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="159ca-116">-Confirm</span></span>
<span data-ttu-id="159ca-117">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="159ca-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="159ca-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="159ca-118">-DefaultProfile</span></span>
<span data-ttu-id="159ca-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="159ca-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="159ca-120">-Name</span><span class="sxs-lookup"><span data-stu-id="159ca-120">-Name</span></span>
<span data-ttu-id="159ca-121">Datenbankname.</span><span class="sxs-lookup"><span data-stu-id="159ca-121">Database name.</span></span>

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

### <span data-ttu-id="159ca-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="159ca-122">-ParentObject</span></span>
<span data-ttu-id="159ca-123">Objekt "Abt.-Konto"</span><span class="sxs-lookup"><span data-stu-id="159ca-123">CosmosDB Account object</span></span>

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

### <span data-ttu-id="159ca-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="159ca-124">-ResourceGroupName</span></span>
<span data-ttu-id="159ca-125">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="159ca-125">Name of resource group.</span></span>

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

### <span data-ttu-id="159ca-126">-Throughput</span><span class="sxs-lookup"><span data-stu-id="159ca-126">-Throughput</span></span>
<span data-ttu-id="159ca-127">Der Durchsatz SQL Datenbank (RU/s).</span><span class="sxs-lookup"><span data-stu-id="159ca-127">The throughput of SQL database (RU/s).</span></span>
<span data-ttu-id="159ca-128">Der Standardwert ist 400.</span><span class="sxs-lookup"><span data-stu-id="159ca-128">Default value is 400.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="159ca-129">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="159ca-129">-WhatIf</span></span>
<span data-ttu-id="159ca-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="159ca-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="159ca-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="159ca-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="159ca-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="159ca-132">CommonParameters</span></span>
<span data-ttu-id="159ca-133">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="159ca-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="159ca-134">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="159ca-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="159ca-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="159ca-135">INPUTS</span></span>

### <span data-ttu-id="159ca-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="159ca-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="159ca-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="159ca-137">OUTPUTS</span></span>

### <span data-ttu-id="159ca-138">Microsoft.Azure.Commands.ExesDB.Models.PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="159ca-138">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="159ca-139">Microsoft.Azure.Commands.DiesDB.Exceptions.ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="159ca-139">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="159ca-140">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="159ca-140">NOTES</span></span>

## <span data-ttu-id="159ca-141">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="159ca-141">RELATED LINKS</span></span>
