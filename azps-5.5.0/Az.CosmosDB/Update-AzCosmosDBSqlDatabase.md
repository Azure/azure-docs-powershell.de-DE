---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlDatabase.md
ms.openlocfilehash: 1c52d1f163f5f5d23f6f282a7f00a071a38761de
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100148465"
---
# <span data-ttu-id="fcf7d-101">Update-AzCosmosDBSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="fcf7d-101">Update-AzCosmosDBSqlDatabase</span></span>

## <span data-ttu-id="fcf7d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fcf7d-102">SYNOPSIS</span></span>
<span data-ttu-id="fcf7d-103">Aktualisiert die Datenbank DestallsDB Sql.</span><span class="sxs-lookup"><span data-stu-id="fcf7d-103">Updates the CosmosDB Sql Database.</span></span> <span data-ttu-id="fcf7d-104">Führt einen clientseitigen Patchvorgang durch, indem die vorhandene Datenbank gelesen wird.</span><span class="sxs-lookup"><span data-stu-id="fcf7d-104">Performs a client side patch operation by reading the existing Database.</span></span>

## <span data-ttu-id="fcf7d-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fcf7d-105">SYNTAX</span></span>

### <span data-ttu-id="fcf7d-106">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="fcf7d-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBSqlDatabase -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fcf7d-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fcf7d-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlDatabase [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fcf7d-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fcf7d-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlDatabase [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -InputObject <PSSqlDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fcf7d-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fcf7d-109">DESCRIPTION</span></span>
<span data-ttu-id="fcf7d-110">Aktualisiert die Datenbank DestallsDB Sql.</span><span class="sxs-lookup"><span data-stu-id="fcf7d-110">Updates the CosmosDB Sql Database.</span></span> <span data-ttu-id="fcf7d-111">Führt einen clientseitigen Patchvorgang durch, indem die vorhandene Datenbank gelesen wird.</span><span class="sxs-lookup"><span data-stu-id="fcf7d-111">Performs a client side patch operation by reading the existing Database.</span></span>

## <span data-ttu-id="fcf7d-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="fcf7d-112">EXAMPLES</span></span>

### <span data-ttu-id="fcf7d-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="fcf7d-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBSqlDatabase -AccountName myAccountName -Name myDatabaseName -ResourceGroupName myResourcegroupName -Throughput 900

Name     : myDatabaseName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/sqlDatabases/myDatabaseName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetPropertiesResource
```

## <span data-ttu-id="fcf7d-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fcf7d-114">PARAMETERS</span></span>

### <span data-ttu-id="fcf7d-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="fcf7d-115">-AccountName</span></span>
<span data-ttu-id="fcf7d-116">Der Name des Dbdatenbankkontos von Db.</span><span class="sxs-lookup"><span data-stu-id="fcf7d-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="fcf7d-117">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="fcf7d-117">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="fcf7d-118">Der maximale Durchsatzwert, wenn die Automatische Skalierung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="fcf7d-118">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="fcf7d-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fcf7d-119">-Confirm</span></span>
<span data-ttu-id="fcf7d-120">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="fcf7d-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fcf7d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fcf7d-121">-DefaultProfile</span></span>
<span data-ttu-id="fcf7d-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fcf7d-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fcf7d-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fcf7d-123">-InputObject</span></span>
<span data-ttu-id="fcf7d-124">Sql-Datenbankobjekt.</span><span class="sxs-lookup"><span data-stu-id="fcf7d-124">Sql Database object.</span></span>

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

### <span data-ttu-id="fcf7d-125">-Name</span><span class="sxs-lookup"><span data-stu-id="fcf7d-125">-Name</span></span>
<span data-ttu-id="fcf7d-126">Datenbankname.</span><span class="sxs-lookup"><span data-stu-id="fcf7d-126">Database name.</span></span>

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

### <span data-ttu-id="fcf7d-127">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="fcf7d-127">-ParentObject</span></span>
<span data-ttu-id="fcf7d-128">Objekt "Abt.-Konto"</span><span class="sxs-lookup"><span data-stu-id="fcf7d-128">CosmosDB Account object</span></span>

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

### <span data-ttu-id="fcf7d-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fcf7d-129">-ResourceGroupName</span></span>
<span data-ttu-id="fcf7d-130">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="fcf7d-130">Name of resource group.</span></span>

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

### <span data-ttu-id="fcf7d-131">-Throughput</span><span class="sxs-lookup"><span data-stu-id="fcf7d-131">-Throughput</span></span>
<span data-ttu-id="fcf7d-132">Der Durchsatz SQL Datenbank (RU/s).</span><span class="sxs-lookup"><span data-stu-id="fcf7d-132">The throughput of SQL database (RU/s).</span></span>
<span data-ttu-id="fcf7d-133">Der Standardwert ist 400.</span><span class="sxs-lookup"><span data-stu-id="fcf7d-133">Default value is 400.</span></span>

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

### <span data-ttu-id="fcf7d-134">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="fcf7d-134">-WhatIf</span></span>
<span data-ttu-id="fcf7d-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fcf7d-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fcf7d-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fcf7d-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fcf7d-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fcf7d-137">CommonParameters</span></span>
<span data-ttu-id="fcf7d-138">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fcf7d-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fcf7d-139">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fcf7d-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fcf7d-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="fcf7d-140">INPUTS</span></span>

### <span data-ttu-id="fcf7d-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="fcf7d-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

### <span data-ttu-id="fcf7d-142">Microsoft.Azure.Commands.ExesDB.Models.PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="fcf7d-142">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

## <span data-ttu-id="fcf7d-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="fcf7d-143">OUTPUTS</span></span>

### <span data-ttu-id="fcf7d-144">Microsoft.Azure.Commands.ExesDB.Models.PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="fcf7d-144">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="fcf7d-145">Microsoft.Azure.Commands.UmsDB.Exceptions.ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="fcf7d-145">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="fcf7d-146">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="fcf7d-146">NOTES</span></span>

## <span data-ttu-id="fcf7d-147">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="fcf7d-147">RELATED LINKS</span></span>
