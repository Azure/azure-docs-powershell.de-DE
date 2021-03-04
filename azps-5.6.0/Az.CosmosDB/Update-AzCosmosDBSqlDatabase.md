---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/update-azcosmosdbsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlDatabase.md
ms.openlocfilehash: 1bfb0ec8392c0ddcce20db839f1817688e8feb7e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101931216"
---
# <span data-ttu-id="b4d1c-101">Update-AzCosmosDBSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="b4d1c-101">Update-AzCosmosDBSqlDatabase</span></span>

## <span data-ttu-id="b4d1c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b4d1c-102">SYNOPSIS</span></span>
<span data-ttu-id="b4d1c-103">Aktualisiert die CosmosDB Sql-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="b4d1c-103">Updates the CosmosDB Sql Database.</span></span> <span data-ttu-id="b4d1c-104">Führt einen clientseitigen Patchvorgang durch Lesen der vorhandenen Datenbank aus.</span><span class="sxs-lookup"><span data-stu-id="b4d1c-104">Performs a client side patch operation by reading the existing Database.</span></span>

## <span data-ttu-id="b4d1c-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b4d1c-105">SYNTAX</span></span>

### <span data-ttu-id="b4d1c-106">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="b4d1c-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBSqlDatabase -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4d1c-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b4d1c-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlDatabase [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b4d1c-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b4d1c-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlDatabase [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -InputObject <PSSqlDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b4d1c-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b4d1c-109">DESCRIPTION</span></span>
<span data-ttu-id="b4d1c-110">Aktualisiert die CosmosDB Sql-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="b4d1c-110">Updates the CosmosDB Sql Database.</span></span> <span data-ttu-id="b4d1c-111">Führt einen clientseitigen Patchvorgang durch Lesen der vorhandenen Datenbank aus.</span><span class="sxs-lookup"><span data-stu-id="b4d1c-111">Performs a client side patch operation by reading the existing Database.</span></span>

## <span data-ttu-id="b4d1c-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b4d1c-112">EXAMPLES</span></span>

### <span data-ttu-id="b4d1c-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b4d1c-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBSqlDatabase -AccountName myAccountName -Name myDatabaseName -ResourceGroupName myResourcegroupName -Throughput 900

Name     : myDatabaseName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/sqlDatabases/myDatabaseName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetPropertiesResource
```

## <span data-ttu-id="b4d1c-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="b4d1c-114">PARAMETERS</span></span>

### <span data-ttu-id="b4d1c-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="b4d1c-115">-AccountName</span></span>
<span data-ttu-id="b4d1c-116">Name des Datenbankkontos "Cosmos DB".</span><span class="sxs-lookup"><span data-stu-id="b4d1c-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="b4d1c-117">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="b4d1c-117">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="b4d1c-118">Maximaler Durchsatzwert, wenn die automatische Skalierung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="b4d1c-118">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="b4d1c-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b4d1c-119">-Confirm</span></span>
<span data-ttu-id="b4d1c-120">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b4d1c-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4d1c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4d1c-121">-DefaultProfile</span></span>
<span data-ttu-id="b4d1c-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b4d1c-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b4d1c-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b4d1c-123">-InputObject</span></span>
<span data-ttu-id="b4d1c-124">Sql Database-Objekt.</span><span class="sxs-lookup"><span data-stu-id="b4d1c-124">Sql Database object.</span></span>

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

### <span data-ttu-id="b4d1c-125">-Name</span><span class="sxs-lookup"><span data-stu-id="b4d1c-125">-Name</span></span>
<span data-ttu-id="b4d1c-126">Datenbankname.</span><span class="sxs-lookup"><span data-stu-id="b4d1c-126">Database name.</span></span>

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

### <span data-ttu-id="b4d1c-127">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="b4d1c-127">-ParentObject</span></span>
<span data-ttu-id="b4d1c-128">CosmosDB-Kontoobjekt</span><span class="sxs-lookup"><span data-stu-id="b4d1c-128">CosmosDB Account object</span></span>

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

### <span data-ttu-id="b4d1c-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4d1c-129">-ResourceGroupName</span></span>
<span data-ttu-id="b4d1c-130">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="b4d1c-130">Name of resource group.</span></span>

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

### <span data-ttu-id="b4d1c-131">-Durchsatz</span><span class="sxs-lookup"><span data-stu-id="b4d1c-131">-Throughput</span></span>
<span data-ttu-id="b4d1c-132">Der Durchsatz SQL Datenbank (RU/s).</span><span class="sxs-lookup"><span data-stu-id="b4d1c-132">The throughput of SQL database (RU/s).</span></span>
<span data-ttu-id="b4d1c-133">Der Standardwert ist 400.</span><span class="sxs-lookup"><span data-stu-id="b4d1c-133">Default value is 400.</span></span>

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

### <span data-ttu-id="b4d1c-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4d1c-134">-WhatIf</span></span>
<span data-ttu-id="b4d1c-135">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b4d1c-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b4d1c-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b4d1c-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4d1c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4d1c-137">CommonParameters</span></span>
<span data-ttu-id="b4d1c-138">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4d1c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4d1c-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b4d1c-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4d1c-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b4d1c-140">INPUTS</span></span>

### <span data-ttu-id="b4d1c-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="b4d1c-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

### <span data-ttu-id="b4d1c-142">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="b4d1c-142">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

## <span data-ttu-id="b4d1c-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b4d1c-143">OUTPUTS</span></span>

### <span data-ttu-id="b4d1c-144">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="b4d1c-144">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="b4d1c-145">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="b4d1c-145">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="b4d1c-146">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="b4d1c-146">NOTES</span></span>

## <span data-ttu-id="b4d1c-147">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="b4d1c-147">RELATED LINKS</span></span>
