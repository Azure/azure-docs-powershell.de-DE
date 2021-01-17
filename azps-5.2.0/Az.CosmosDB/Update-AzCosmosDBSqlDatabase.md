---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlDatabase.md
ms.openlocfilehash: 1c52d1f163f5f5d23f6f282a7f00a071a38761de
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98372965"
---
# <span data-ttu-id="39fba-101">Update-AzCosmosDBSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="39fba-101">Update-AzCosmosDBSqlDatabase</span></span>

## <span data-ttu-id="39fba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="39fba-102">SYNOPSIS</span></span>
<span data-ttu-id="39fba-103">Aktualisiert die Datenbank DestallsDB Sql.</span><span class="sxs-lookup"><span data-stu-id="39fba-103">Updates the CosmosDB Sql Database.</span></span> <span data-ttu-id="39fba-104">Führt einen clientseitigen Patchvorgang durch, indem die vorhandene Datenbank gelesen wird.</span><span class="sxs-lookup"><span data-stu-id="39fba-104">Performs a client side patch operation by reading the existing Database.</span></span>

## <span data-ttu-id="39fba-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="39fba-105">SYNTAX</span></span>

### <span data-ttu-id="39fba-106">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="39fba-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBSqlDatabase -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="39fba-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="39fba-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlDatabase [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="39fba-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="39fba-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlDatabase [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -InputObject <PSSqlDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="39fba-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="39fba-109">DESCRIPTION</span></span>
<span data-ttu-id="39fba-110">Aktualisiert die Datenbank DestallsDB Sql.</span><span class="sxs-lookup"><span data-stu-id="39fba-110">Updates the CosmosDB Sql Database.</span></span> <span data-ttu-id="39fba-111">Führt einen clientseitigen Patchvorgang durch, indem die vorhandene Datenbank gelesen wird.</span><span class="sxs-lookup"><span data-stu-id="39fba-111">Performs a client side patch operation by reading the existing Database.</span></span>

## <span data-ttu-id="39fba-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="39fba-112">EXAMPLES</span></span>

### <span data-ttu-id="39fba-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="39fba-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBSqlDatabase -AccountName myAccountName -Name myDatabaseName -ResourceGroupName myResourcegroupName -Throughput 900

Name     : myDatabaseName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/sqlDatabases/myDatabaseName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetPropertiesResource
```

## <span data-ttu-id="39fba-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="39fba-114">PARAMETERS</span></span>

### <span data-ttu-id="39fba-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="39fba-115">-AccountName</span></span>
<span data-ttu-id="39fba-116">Der Name des Dbdatenbankkontos von Db.</span><span class="sxs-lookup"><span data-stu-id="39fba-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="39fba-117">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="39fba-117">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="39fba-118">Der maximale Durchsatzwert, wenn die Automatische Skalierung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="39fba-118">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="39fba-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="39fba-119">-Confirm</span></span>
<span data-ttu-id="39fba-120">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="39fba-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="39fba-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39fba-121">-DefaultProfile</span></span>
<span data-ttu-id="39fba-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="39fba-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="39fba-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="39fba-123">-InputObject</span></span>
<span data-ttu-id="39fba-124">Sql-Datenbankobjekt.</span><span class="sxs-lookup"><span data-stu-id="39fba-124">Sql Database object.</span></span>

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

### <span data-ttu-id="39fba-125">-Name</span><span class="sxs-lookup"><span data-stu-id="39fba-125">-Name</span></span>
<span data-ttu-id="39fba-126">Datenbankname.</span><span class="sxs-lookup"><span data-stu-id="39fba-126">Database name.</span></span>

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

### <span data-ttu-id="39fba-127">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="39fba-127">-ParentObject</span></span>
<span data-ttu-id="39fba-128">Objekt "Abt.-Konto"</span><span class="sxs-lookup"><span data-stu-id="39fba-128">CosmosDB Account object</span></span>

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

### <span data-ttu-id="39fba-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39fba-129">-ResourceGroupName</span></span>
<span data-ttu-id="39fba-130">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="39fba-130">Name of resource group.</span></span>

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

### <span data-ttu-id="39fba-131">-Throughput</span><span class="sxs-lookup"><span data-stu-id="39fba-131">-Throughput</span></span>
<span data-ttu-id="39fba-132">Der Durchsatz SQL Datenbank (RU/s).</span><span class="sxs-lookup"><span data-stu-id="39fba-132">The throughput of SQL database (RU/s).</span></span>
<span data-ttu-id="39fba-133">Der Standardwert ist 400.</span><span class="sxs-lookup"><span data-stu-id="39fba-133">Default value is 400.</span></span>

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

### <span data-ttu-id="39fba-134">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="39fba-134">-WhatIf</span></span>
<span data-ttu-id="39fba-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="39fba-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="39fba-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="39fba-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="39fba-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39fba-137">CommonParameters</span></span>
<span data-ttu-id="39fba-138">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39fba-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39fba-139">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="39fba-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39fba-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="39fba-140">INPUTS</span></span>

### <span data-ttu-id="39fba-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="39fba-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

### <span data-ttu-id="39fba-142">Microsoft.Azure.Commands.ExesDB.Models.PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="39fba-142">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

## <span data-ttu-id="39fba-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="39fba-143">OUTPUTS</span></span>

### <span data-ttu-id="39fba-144">Microsoft.Azure.Commands.ExesDB.Models.PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="39fba-144">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="39fba-145">Microsoft.Azure.Commands.Abt. Exceptions.ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="39fba-145">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="39fba-146">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="39fba-146">NOTES</span></span>

## <span data-ttu-id="39fba-147">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="39fba-147">RELATED LINKS</span></span>
